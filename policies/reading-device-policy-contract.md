# Reading Device & Emoji Policy Contract

Canonical field: `reading_device_policy` (string). Accepted values: `MOBILE_STORY`, `MOBILE_FIRST`, `DESKTOP_FIRST`, `BALANCED`; default and unknown-value fallback: `BALANCED`.

Independent optional field: `emoji_policy` (string). Accepted values: `NONE`, `SPARING`, `EXPRESSIVE`; default and unknown-value fallback: `NONE`. Do not infer emoji mode from reading-device mode.

MOBILE_STORY has an editorial line-length rule: maximum 24 displayed characters per prose line, with semantic breaks and documented exceptions for unbreakable strings. Other modes have no line-length cap.

These are **advisory editorial preferences**, not new Case statuses, ranking factors, or required fields in existing article output schemas. SBM owns the site settings and change history. Consuming products use `knowledge/reading-device-editorial-policy.md` for editorial behavior.

Never initiate a bulk rewrite, monitoring reset, or automatic publication because of a policy change. Preserve existing approval gates, evidence requirements, and product-specific responsibility boundaries.
