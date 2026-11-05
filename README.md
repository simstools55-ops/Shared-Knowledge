## v3.6.4 — MOBILE_STORY and emoji policy

Adds fourth reading style and independent emoji preferences; backwards-compatible defaults.

# Shared Knowledge v3.6.1

SIMS Editorial PlatformのKnowledge and Contract Planeであり、共通Contract、Enum、編集知識、Validation、製品責務境界の唯一の正本です。

## Platform構成

```text
SIMS Manager -> aDoctor -> SIMS Manager -> aWriter / aCreator / aMerge -> SIMS Manager -> publication -> monitoring -> re-examination
```

- SIMS Manager（内部コード: SBM）：Control Plane、Case・状態・Routing・効果測定の正本
- aDoctor（内部契約名: Article Doctor / DOCTOR）：診断、原因仮説、Treatment Plan、Referral
- aWriter（内部契約名: Writer）：既存記事の治療
- aCreator（内部契約名: Creator）：新記事作成と検索意図分離
- aMerge（内部契約名: Merge）：複数記事の統合・役割整理・高リスク処置計画
- Shared Knowledge：Contract、Enum、共通知識、Validation、Governance

## 主要Directory

```text
architecture/   Platform設計と運用
contracts/      canonical Contract schemaとAdapter
knowledge/      共通知識・製品別知識
validation/     共通Validation
patterns/       編集Pattern
quality/        品質契約
mappings/       Writer／Creator適用Mapping
doctor/         Article Doctor Case・Routing互換仕様
enums/          Platform共通Enum
snapshots/      Product-scoped Snapshot定義
```

## 利用原則

1. 共通Contract・Enum・横断ルールはこのRepositoryだけで変更します。
2. 各製品はRelease済みSharedからProduct-scoped Snapshotを生成します。
3. aDoctorから専門製品へ直接依頼せず、すべてSIMS Managerを経由します。
4. Case状態を確定できるのはSIMS Managerだけです。
5. 削除・noindex・Redirect・統合など高リスク処置は利用者判断を必須とします。

## Version

`3.6.1`

Platform compatibility: `SIMS Editorial Platform 1.x`


## Human Experience / Presentation

`presentation/` defines the common Human Experience Architecture for SIMS Manager, aDoctor, aWriter, aCreator, and aMerge. Machine contracts remain detailed; human-facing output must be actionable and must follow the Presentation Standard.

## Reading device editorial policy

`knowledge/reading-device-editorial-policy.md` and `policies/reading-device-policy-contract.md` define the site-level three-mode editorial preference and safe fallback. Product-scoped integrations must explicitly consume the released policy; updating Shared alone does not change installed Claude projects.
