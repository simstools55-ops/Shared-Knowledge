# Shared Knowledge v3.6.0 Release Notes

## Product terminology consolidation

- Human-facing platform terminology is standardized to SIMS Manager, aDoctor, aWriter, aCreator, aMerge, Site Collector, Site Doctor, Keyword Explorer, Blue Ocean Screener, Shared Knowledge, and Personal Knowledge.
- Existing machine contracts, enum values, product codes, schema identifiers, repository identifiers, and compatibility names are preserved.
- PRODUCT_IDENTITY adds `display_name` without changing canonical `product_name`.
- PLATFORM_MANIFEST adds an additive `product_display_names` registry.
- README version drift is corrected from 3.5.1 to 3.6.0.

This release changes presentation/governance terminology only; it does not revise canonical machine contracts.
