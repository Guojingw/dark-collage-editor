---
name: dark-collage-editor
description: "Transform user-supplied portrait photos into dark collage / punk / goth / emo / zine editorial artwork while strictly preserving the original person. Use when the user wants black / deep-red / dirty-white torn-paper collage, xerox texture, graffiti, distressed typography, or a coherent portrait series. Preserve identity, pose, hands, clothes, jewelry, camera angle, and original orientation; rebuild the surrounding design rather than merely adding a border."
---

# Dark Collage Editor v2

Create a finished dark editorial collage from the user's own portrait photo(s).

The signature is:

**人物真实保留 + 背景重新设计 + 黑/深红/脏白大结构 + 撕纸/复印/zine 材质 + 克制的人像碎片。**

The result should feel like the original person was art-directed into a punk / goth / zine editorial page, not like a new AI person and not like the original photo with a decorative border.

## 1. Non-negotiable identity lock

Unless the user explicitly asks otherwise, preserve:

- identity and face
- facial proportions and defining features
- hairstyle
- expression
- body pose
- hand pose
- clothing
- accessories and jewelry
- camera angle
- original horizontal / vertical orientation

Do **not** beautify, reconstruct, replace, restyle, or redesign the main face merely to fit the aesthetic.

Do **not** invent new hands, extra limbs, new jewelry, different clothes, or a new hairstyle.

The source portrait is factual. The surrounding graphic design is flexible.

## 2. Use image editing, not filter simulation

When image editing / generation is available, use it directly on the supplied photo.

Do not simulate the finished dark collage with Python, PIL, simple filters, border overlays, or a procedural texture pass.

Those tools may be used only for measurement, inspection, contact sheets, or non-creative utility work. They are not a substitute for the actual edit.

A result that is only:

- source photo + border
- source photo + grain
- source photo + red scratches
- source photo + dark vignette

is a failure.

## 3. Default behavior

If the user simply asks for dark collage style, use:

- Preset: **Editorial**
- Readable text: **None**
- Identity preservation: **Strict**
- Orientation: **Preserve**
- Portrait fragments: **0–1 by default**
- Batch mode: **Consistent series, varied layouts**

Do not force the user to write a technical prompt.

Ask at most these only when genuinely missing:

1. Clean / Editorial / Chaotic?
2. Exact text, or no readable text?
3. For multiple photos: consistent series or stronger variation?

If these are already clear, edit immediately.

## 4. Read the portrait before designing

Before generating, build an internal **Portrait Design Card**.

Resolve:

- **Hero subject:** where the person is and how much visual weight they carry.
- **Identity-critical zones:** face, hands, hairstyle, jewelry, distinctive clothing details.
- **Pose vector:** dominant body / arm / gaze direction.
- **Background freedom:** which source background areas can be removed, covered, or retained.
- **Negative-space zones:** safe areas for typography, torn paper, halftone, paint, or graphic fields.
- **Cutout potential:** full subject cutout, partial separation, or photo-field retention.
- **Source fragment candidate:** eye / half-face / hand / profile / none.
- **Graphic pressure point:** the one area where the main collage collision should occur.
- **Native color:** meaningful source colors worth preserving in skin, clothes, or jewelry.
- **Batch role:** if multiple photos, what visual role this image should play in the series.

Do not show this analysis unless the user asks.

## 5. Decision priority

When rules conflict, resolve them in this order:

1. Preserve the actual person.
2. Preserve pose, hands, clothes, jewelry, angle, and orientation.
3. Keep the person as the first visual read.
4. Make the composition materially different from the source photograph.
5. Use one clear macro composition instead of random decoration.
6. Use source-derived portrait fragments only when useful.
7. Keep black / deep red / dirty white coherent.
8. Add texture only after the macro design works.
9. Preserve readable text exactly when the user supplies it.
10. Keep batch outputs related without template duplication.

## 6. Choose one composition family

Read `references/composition-families.md`.

For every image, choose **one primary composition family** based on the source portrait.

Do not mix all families together.

The main families are:

- A — Hero Cutout
- B — Split Photography
- C — Oversized Type Field
- D — Torn Portrait Collision
- E — Graphic Negative Space
- F — Tight Crop Poster

The composition family should come from the portrait geometry, not from habit.

For a batch, distribute families intentionally so adjacent outputs do not feel copy-pasted.

## 7. Build with three visual scales

Do not use a checklist that forces every possible punk element into every image.

### Macro layer — choose 1–2
Large structural moves:

- black field
- dirty-white torn field
- deep-red structural shape
- oversized cropped typography
- major diagonal / vertical tear
- large photocopy / halftone block

### Meso layer — choose 2–3
Supporting design moves:

- one source-photo portrait fragment
- tape
- red dry-brush stroke
- xerox patch
- chain / cross / safety-pin-like hardware motif
- medium halftone patch
- torn-paper overlap
- one graphic label

### Micro layer — choose 2–4
Surface detail:

- scratches
- grain
- paper fibers
- tiny X / star / heart / arrow
- ink speckle
- faint pencil / chalk marks
- minor misregistration
- distressed print residue

Macro structure must work before meso and micro detail are added.

## 8. Palette and material system

Read `references/style-guide.md`.

Default graphic palette:

- black / charcoal: dominant
- deep red / oxblood / dark wine: accent
- dirty white / off-white / photocopy gray: contrast
- natural skin and meaningful garment / jewelry colors: preserved where useful

For Editorial / Chaotic, the **redesigned background region** should usually be visually dominated by black, then dirty white / gray, then deep red.

Do not mechanically recolor the person's skin, clothes, or jewelry to match a percentage.

Avoid a global warm-brown / sepia filter unless the user asks for it.

## 9. Torn paper must be compositional

Torn paper is not a border.

At least one major tear or paper field should:

- enter the image interior,
- separate photography from graphic space,
- pass behind or around the subject,
- redirect the eye,
- create a large black / white division,
- or break the original photographic frame.

Avoid equal torn borders on all four sides.

## 10. Source-only portrait fragments

Any added face, eye, mouth, hand, profile, or portrait crop must come from the user's supplied source photo(s).

Never invent:

- extra eyes
- unrelated faces
- look-alike portraits
- decorative stranger hands

If source reuse cannot be guaranteed, omit the portrait fragment.

Use graphic material instead.

Recommended limits:

- Clean: 0–1
- Editorial: 0–2, usually 0–1
- Chaotic: 1–3 maximum

**Chaotic means denser graphics, not more repeated faces.**

## 11. Typography

If the user supplies exact text:

- reproduce it exactly
- preserve capitalization
- use the main phrase once by default
- keep it away from defining eyes, nose, and mouth unless the user explicitly wants overlap

Typography should function as a graphic mass, not filler copy.

If the user says **No text / 不要文字**:

Do not invent readable phrases, headlines, slogans, magazine copy, or motivational English.

Allowed:

- cropped letter fragments
- illegible blackletter texture
- blurred xerox type
- newspaper-like texture
- abstract letterforms
- isolated symbols

These must not accidentally form a new readable slogan.

## 12. Presets

### Clean
Photography first.

- portrait attention: 80–90%
- 0–1 portrait fragment
- one restrained macro move
- light torn paper
- restrained red
- moderate grain
- generous negative space

### Editorial — default
Balanced portrait and design.

- portrait attention: 70–85%
- 0–2 portrait fragments
- clear background reconstruction
- 1–2 macro moves
- 2–3 meso moves
- visible xerox / halftone / torn-paper language
- asymmetric editorial hierarchy
- deliberate negative space

### Chaotic
Aggressive poster / DIY zine energy while keeping identity clear.

- portrait attention: 60–80%
- 1–3 portrait fragments maximum
- stronger macro collisions
- more torn paper, red gesture, scratches, xerox, and typography
- less negative space
- still one clear focal subject

Do not create chaos by multiplying heads.

## 13. Batch / series mode

For two or more images, first build an internal **Series Plan**.

Lock across the series:

- black / red / off-white family
- red hue
- paper family
- xerox / grain character
- contrast philosophy
- typography family
- overall emotional tone

Vary across images:

- composition family
- subject placement
- macro tear direction
- red shape direction
- amount of negative space
- use / non-use of portrait fragment
- typography scale and placement
- halftone location
- crop intensity

Avoid using the same family on every image.

A good batch should feel like pages from the same zine, not one template with different photographs.

## 14. Reference images

When style references are supplied, treat them as the main visual-language target after identity preservation and the user's current request.

Study:

- collage density
- black / red / white balance
- scale of torn shapes
- amount of background replacement
- xerox texture
- graffiti density
- type energy
- negative space
- subject cutout treatment
- hierarchy

Do not copy the exact layout of a reference image.

Aim for:

**same visual language, different composition.**

## 15. Prompt compiler

Before calling the image editor, compile only pixel-visible instructions.

The generation instruction should resolve, in this order:

1. Preserve the exact supplied person and orientation.
2. State which source areas must stay unchanged.
3. State the selected composition family.
4. State what happens to the original background.
5. State the macro layer.
6. State the meso layer.
7. State the micro texture layer.
8. State palette and material.
9. State source-only portrait-fragment behavior.
10. State exact text or no-readable-text behavior.
11. State batch continuity when applicable.
12. State hard avoids.

Do not dump design theory, file paths, or hidden analysis into the image prompt.

## 16. Quality gate

After generation, inspect the result against `references/quality-gate.md`.

Regenerate **once** before presenting if any critical failure occurs, especially:

- identity drift
- altered pose / hand / clothing
- changed orientation
- invented face or portrait fragment
- random readable text
- border-only treatment
- original background still dominates in Editorial / Chaotic
- no internal graphic collision
- chaotic clutter with no hierarchy
- same layout duplicated within the batch

If a second attempt still cannot preserve identity, simplify the collage rather than pushing style harder.

## 17. Output behavior

When editing tools are available:

- perform the image edit directly
- preserve the user's already-stated preferences across the batch
- do not make the user rewrite the prompt for every photo
- do not precede the edit with a long explanation
- show the result first

If the user asks for rationale, prompt details, or composition notes, provide them after the image result.

## 18. One-line definition

**Preserve the real person strictly, choose one source-aware poster composition, rebuild the surrounding space with black / deep-red / dirty-white torn-paper and xerox structure, use only sparse source-derived portrait fragments, and reject any result that reads as a border/filter treatment or an AI look-alike.**
