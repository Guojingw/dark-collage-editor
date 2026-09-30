# Dark Collage Editor / 暗黑拼贴编辑器

A source-faithful portrait editing workflow for dark collage / punk / goth / emo / zine editorial artwork.

The project is designed around one rule:

**Preserve the real target person. Rebuild the surrounding design.**

## v3 architecture

The repository now has one canonical Skill plus Project-compatible files.

### Skill mode
Use:
- SKILL.md
- references/style-guide.md
- references/composition-families.md
- references/quality-gate.md

### ChatGPT Project mode
Use:
- PROJECT_INSTRUCTIONS.md
- STYLE_GUIDE.md
- optionally upload the three files under references/ for stronger behavior
- add 3–6 non-private style reference images if desired

## What v3 fixes

Compared with earlier versions, v3 explicitly separates:

- **TARGET** photos — identity and body content come from here
- **STYLE_REFERENCE** images — visual language only
- **SERIES_REFERENCE** images — continuity only

This prevents a common failure where the model borrows another person's face, eye, hand, hair, outfit, or pose from a style reference.

v3 also adds:

- Portrait Design Card before generation
- source-aware composition-family selection
- Macro / Meso / Micro structure budget
- same-TARGET portrait-fragment rule
- face / hand occlusion rules
- style-reference contamination checks
- automatic one-pass recovery when generation fails
- stronger batch anti-template rules

## Default behavior

If the user only asks for dark collage style:

- preset: Editorial
- readable text: none
- identity preservation: strict
- orientation: preserve
- portrait fragments: 0–1
- batch: coherent series with varied layouts

## Example request

> Images 1–3 are style references. Edit images 4–9 as one Editorial series. No readable text. Keep my face, pose, hands, clothes, jewelry and original orientation. Use the references only for visual language, not for people or portrait fragments.

中文：

> 1–3 是风格参考图，帮我把 4–9 做成同一个 Editorial 系列。不要可读文字。严格保留我的脸、动作、手、衣服、首饰和原始横竖方向。参考图只学习视觉语言，不能借人物或人像碎片。

## Visual signature

- black / charcoal as the main graphic mass
- oxblood / dark wine red as structural accent
- dirty white / photocopy gray as contrast
- hand-torn paper
- xerox / halftone
- distressed print
- controlled scratches / tape / hardware
- sparse portrait fragments
- strong internal composition, not decorative borders

## Test

Use TEST_CASES.md.

The most important v3 tests are:

1. identity preservation
2. style-reference contamination
3. border-only failure
4. same-target fragment authenticity
5. exact / no-text behavior
6. batch layout diversity

## No-code setup

See START_HERE.md.

## License

MIT.
