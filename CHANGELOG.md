# Changelog

## v3.0 — Source-aware skill architecture

- Made SKILL.md the canonical workflow while keeping ChatGPT Project compatibility.
- Added explicit TARGET / STYLE_REFERENCE / SERIES_REFERENCE role classification.
- Added a hard ban on borrowing faces, eyes, hands, hair, clothes, jewelry, poses, or portrait fragments from style references.
- Added a Portrait Design Card and Style Vector extraction step before generation.
- Reworked composition into six source-aware families instead of generic template reuse.
- Replaced element-count styling with Macro / Meso / Micro structure budgets.
- Changed portrait fragments to same-TARGET by default.
- Added face / hand occlusion rules.
- Strengthened No text vs No readable text behavior.
- Added reference-contamination, interior-collision, thumbnail, and batch anti-template quality checks.
- Added one-pass recovery logic when a generated result fails.
- Expanded smoke tests and setup documentation for reference-heavy and batch workflows.

## Project-first beta

- Reframed Dark Collage Editor as a no-code ChatGPT Project workflow.
- Removed Plugin / Skill packaging from the main branch.
- Added a copy-ready Project Instructions file.
- Added a separate visual Style Guide.
- Added a 5-minute first-run setup guide.
- Added repeatable smoke tests for identity preservation, no-text behavior, exact typography and batch consistency.
- Kept the original Plugin / Skill prototype in Git history rather than requiring users to install it.

## v0.2.0 — Skill / Plugin prototype

- Added skills-only Plugin packaging.
- Added Clean / Editorial / Chaotic presets.
- Added source-photo authenticity rules.
- Added batch series rules.

## v0.1.0

- Initial reusable style workflow.
