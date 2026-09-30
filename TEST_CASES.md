# Dark Collage Editor v3 — Smoke Tests
# 暗黑拼贴编辑器 v3 — 基础测试

Use the same source image and prompt when comparing revisions. Test identity first, then style strength, then batch consistency.

## Test 01 — Single image / 单张无文字

User:
> Editorial. No text. Preserve my face, pose, hands, clothes, jewelry and original orientation.

Pass:
- same person
- same pose and hands
- clothes / jewelry unchanged
- orientation unchanged
- no readable words or letters
- background clearly redesigned
- at least one Macro structure enters the image interior
- result is not just border + grain

## Test 02 — Style references must not leak / 参考图人物不能混入

Input:
- 1–3 STYLE_REFERENCE images containing another person
- 1 TARGET portrait

User:
> Images 1–3 are style references only. Edit image 4 in the same visual language. Editorial. No readable text.

Pass:
- output person comes only from TARGET
- no reference face / eye / hand / hair / outfit / pose appears
- reference influences palette, tear scale, xerox, density and hierarchy only
- layout is source-specific rather than copied exactly

Critical fail:
- any human feature from reference images appears

## Test 03 — Exact custom text / 精确文字

User:
> Editorial. Text: STAY IN THE NOISE. Use it once. Do not cover my face.

Pass:
- exact spelling and capitalization
- phrase appears once as primary readable text
- no additional invented slogan
- face remains unobstructed
- identity / pose remain stable

## Test 04 — No readable text vs no text

A:
> Editorial. No text.

Expected:
- no words
- no letters
- no fake magazine copy

B:
> Editorial. No readable text. Abstract distressed letter fragments are okay.

Expected:
- no readable phrase
- abstract letter fragments may appear sparingly

## Test 05 — Strong Editorial / 不允许边框式假拼贴

User:
> Editorial. No readable text. Make the background substantially dark-zine while keeping me unchanged.

Pass:
- one dominant Macro field / tear / xerox structure
- black / oxblood / dirty-white relationship is obvious
- original background is materially transformed
- collage enters the interior
- person remains first visual read

Fail:
- original photo stays intact with only side borders, grain, scratches or corner decoration

## Test 06 — Same-target fragment authenticity / 人像碎片来源

User:
> Editorial. Use at most one portrait fragment, and it must come from this exact photo.

Pass:
- at most one fragment
- fragment is recognizably derived from same TARGET
- if exact reuse cannot be maintained, no portrait fragment is used
- no invented alternate face

## Test 07 — Chaotic without face spam

User:
> Chaotic. No readable text. Make it aggressive with torn paper, oxblood paint, xerox, scratches and graffiti, but do not repeat my face.

Pass:
- denser than Editorial
- macro structure remains clear
- no wall of faces
- no stranger portrait fragment
- chaos comes from graphics / material, not duplicated portraits

## Test 08 — Batch series / 批量系列

Upload 4–9 TARGET photos.

User:
> Make these one coherent Editorial series. No readable text. Keep the palette and material language consistent, but make every page composition different.

Pass:
- same red hue / paper / xerox family
- at least three distinct macro geometries when source set permits
- adjacent pages do not mechanically repeat the same composition family
- fragment use varies
- page density varies
- each image preserves original orientation
- series feels related, not templated

## Test 09 — Horizontal negative-space source

User:
> Editorial. No text. Preserve the horizontal composition.

Pass:
- stays horizontal
- does not force a centered portrait
- graphic field uses existing gaze / arm / negative-space direction
- no decorative perimeter frame

## Test 10 — Tight face crop

User:
> Editorial. No readable text. Keep my face completely recognizable.

Pass:
- eyes / nose / mouth unchanged
- no halftone or tear covers defining face features
- strongest graphics occur at edge / hair / shoulder / background
- skin is not rebuilt or over-smoothed

## Failure log

Record only the observed failure and change the smallest relevant rule.

Categories:
- identity drift
- hand / pose drift
- clothes / jewelry drift
- orientation changed
- style-reference contamination
- invented portrait fragment
- random readable text
- exact text wrong
- border-only treatment
- style too weak
- micro clutter
- face over-occluded
- batch template repetition
- palette drift
- other

Template:

Test:
TARGET:
STYLE_REFERENCE:
Preset:
Observed:
Expected:
Failure category:
One rule to change:
