# Start Here / 从这里开始

## Recommended setup / 推荐配置

Dark Collage Editor v3 can be used in two ways:

1. **Skill mode** — recommended when your environment supports SKILL.md + references.
2. **ChatGPT Project mode** — easiest no-code setup.

---

## A. Skill mode / Skill 模式

Use these files together:

- SKILL.md
- references/style-guide.md
- references/composition-families.md
- references/quality-gate.md

SKILL.md is the canonical workflow.

The reference files provide:
- visual grammar
- source-aware layout families
- post-generation quality checks

Do not merge all four files into one giant prompt unless your environment requires it.

---

## B. ChatGPT Project mode / Project 模式

You do not need:
- Codex CLI
- Node.js
- Python
- API key
- plugin installation

### Step 1 — Create a fresh Project

Create a Project such as:

**Dark Collage Editor — v3**

Use a fresh Project when testing new instruction revisions.

### Step 2 — Add Project Instructions

Copy the full contents of:

**PROJECT_INSTRUCTIONS.md**

into the Project Instructions field.

### Step 3 — Upload support files

Recommended uploads:

- STYLE_GUIDE.md
- references/composition-families.md
- references/quality-gate.md

If the Project reliably reads SKILL.md as a file, you may also upload it for reference, but PROJECT_INSTRUCTIONS.md remains the direct Project instruction source.

### Step 4 — Add style reference images

Optional but recommended: 3–6 non-private reference images.

A useful reference set may include:
- 1 close-up
- 1 full / half-body
- 1 horizontal composition
- 1 strong typography example
- 1 no-text example
- 1 quieter editorial page

Do not upload private originals to a public GitHub repository.

Reference images are **STYLE_REFERENCE only** unless the user explicitly says otherwise.

They must never donate:
- faces
- eyes
- hands
- hair
- clothes
- jewelry
- body parts
- portrait fragments

### Step 5 — First real test

Upload:
- 1–3 style references
- 1 target portrait

Then send:

> Images 1–3 are style references only. Edit image 4 in Editorial style. No readable text. Preserve my face, pose, hands, clothes, jewelry and original orientation.

中文：

> 1–3 是风格参考图，只参考视觉语言。帮我修第 4 张，Editorial，不要可读文字。严格保留我的脸、动作、手、衣服、首饰和原始横竖方向。

Check against TEST_CASES.md Test 02 and Test 05.

---

## Batch test / 批量测试

Upload 4–9 TARGET photos plus optional style references.

Use:

> Make the target photos one coherent Editorial series. No readable text. Keep the red hue, paper, xerox texture and overall mood consistent, but use different source-aware compositions for each image. Do not borrow people or portrait fragments from style references.

中文：

> 把这些 TARGET 照片做成同一个 Editorial 系列。不要可读文字。统一红色色调、纸张、xerox 纹理和整体气质，但每张根据原图使用不同构图。绝对不要从参考图借人物或人像碎片。

---

## What success looks like / 成功标准

A successful result should have:

- same person
- same face
- same pose
- same hands
- same clothes / jewelry
- same orientation
- no style-reference person contamination
- one clear macro graphic idea
- collage entering the image interior
- black / oxblood / dirty-white visual hierarchy
- no unwanted readable text
- source-authentic fragments only
- batch consistency without template repetition

A failed result often looks like:

- original photo + border
- original photo + grain
- random red scratches
- another person's eye / face appears
- face becomes an AI look-alike
- all batch pages use the same layout
- random English is invented

---

## If a test fails / 测试失败怎么办

Do not rewrite everything.

Use TEST_CASES.md to classify the failure.

Then change the smallest relevant rule.

Examples:

- face changed → strengthen portrait lock or simplify overlap
- reference person's eye appears → strengthen STYLE_REFERENCE contamination ban
- style too weak → strengthen Macro structure, not Micro clutter
- too messy → remove Micro first
- batch repetitive → change composition-family distribution
- border-only → require an interior collision and stronger background reconstruction

Always retest with the same source image and prompt when comparing instruction versions.
