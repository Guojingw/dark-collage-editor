---
name: dark-collage-editor
description: "Transform user-supplied portrait photos into dark collage / punk / goth / emo / zine editorial artwork while strictly preserving the target person. Use for black / oxblood / dirty-white torn-paper collage, xerox/halftone texture, distressed type, graffiti, and coherent multi-photo portrait series. Treat style references as style-only and never borrow their people, faces, clothes, or body parts."
---

# Dark Collage Editor v3

Create a finished dark editorial collage from the user's own portrait photo(s).

Core signature:

**strict portrait fidelity + source-aware recomposition + black / oxblood / dirty-white macro structure + torn-paper / xerox / zine material + sparse source-authentic fragments.**

The result should look like the user's real photograph was art-directed into a punk / goth / zine editorial page. It must not look like a newly generated look-alike, a filter pass, or a decorated border.

## 1. Input roles come first

Before editing, classify every supplied image into one role:

- **TARGET** — the photo being edited. Identity, pose, clothes, hands, jewelry, camera angle, and orientation come from this image.
- **STYLE_REFERENCE** — used only for palette, density, torn-paper scale, typography energy, texture, visual hierarchy, and composition language.
- **SERIES_REFERENCE** — a previous finished output used only to keep the current batch visually consistent.

Never treat a STYLE_REFERENCE as a donor image.

Do not borrow from a STYLE_REFERENCE:
- face
- eye
- mouth
- hand
- hair
- clothes
- jewelry
- body
- pose
- portrait fragment

If the user says “1–3 are references” or equivalent, infer those roles directly and do not ask again.

For batch editing, each output should use its own TARGET image as the portrait source by default.

## 2. Non-negotiable portrait lock

Unless the user explicitly requests a change, preserve from the TARGET:

- identity
- face shape and facial proportions
- defining eyes, nose, mouth, brows, and skin structure
- hairstyle and hairline
- expression
- body pose
- hand pose and finger count
- clothing
- accessories and jewelry
- camera angle and perspective
- original horizontal / vertical orientation

Do not beautify, reconstruct, replace, restyle, or “improve” the main face to fit the aesthetic.

Do not invent new hands, limbs, jewelry, clothes, hairstyle, tattoos, piercings, or makeup details.

The portrait is factual. The surrounding design is flexible.

## 3. Use image editing, not procedural imitation

When image editing / generation is available, use it directly on the TARGET image.

Do not use Python, PIL, simple filters, procedural borders, or texture overlays as the final creative method.

Utility code may be used only for inspection, measurements, contact sheets, or file handling.

These are automatic failures:
- source photo + border
- source photo + grain
- source photo + red scratches
- source photo + vignette
- source photo + a few decorative stickers

The design must materially recompose the image.

## 4. Read the target before designing

Build an internal **Portrait Design Card** for each TARGET:

- **Hero region** — where the person sits and their visual weight.
- **Identity-critical zones** — face, hands, hairline, jewelry, distinctive clothing.
- **Pose vector** — body, arm, gaze, and dominant directional gesture.
- **Background freedom** — which source areas may be removed, obscured, or retained.
- **Negative-space zones** — safe regions for type, torn paper, halftone, paint, or large fields.
- **Cutout potential** — full subject cutout, partial separation, or photo-field retention.
- **Pressure point** — one place where the strongest graphic collision should occur.
- **Fragment candidate** — eye / half-face / hand / profile / none.
- **Native color anchors** — source colors worth preserving.
- **Series role** — if part of a batch, what makes this page different from the others.

Do not show this internal card unless the user asks.

## 5. Extract a Style Vector from references

When STYLE_REFERENCE images are supplied, extract only:

- black / red / off-white balance
- collage density
- dominant tear scale and direction
- amount of source-background replacement
- xerox / halftone intensity
- typography scale and aggression
- red gesture behavior
- paper / print material
- amount of negative space
- subject-to-graphics relationship

Then adapt that language to the TARGET geometry.

Do not copy a reference layout literally.

Aim for:

**same visual language, source-specific composition.**

## 6. Decision priority

Resolve conflicts in this order:

1. Preserve the real TARGET person.
2. Preserve pose, hands, clothes, jewelry, angle, and orientation.
3. Prevent contamination from STYLE_REFERENCE people.
4. Keep the person as the first visual read.
5. Make the composition materially different from the source photo.
6. Choose one clear macro composition from the TARGET geometry.
7. Use source-authentic portrait fragments only when needed.
8. Match the reference Style Vector.
9. Add meso and micro texture only after macro structure works.
10. Preserve exact user-supplied text.
11. Keep a batch coherent without template repetition.

## 7. Choose one primary composition family

Read references/composition-families.md.

Choose exactly one primary family per output:

- A — Hero Cutout
- B — Split Photography
- C — Oversized Type Field
- D — Torn Portrait Collision
- E — Graphic Negative Space
- F — Tight Crop Poster

One optional secondary device may support it, but do not merge several families equally.

Select the family from:
- portrait scale
- pose direction
- negative space
- background usefulness
- orientation
- reference Style Vector

For a batch, vary the family and macro geometry intentionally.

## 8. Structure budget: Macro → Meso → Micro

Do not force a long checklist of punk elements into every image.

### Macro — 1 dominant + at most 1 counterweight
Use large structural moves:
- black field
- dirty-white torn field
- oxblood / deep-red structural shape
- oversized cropped typography
- major diagonal / vertical tear
- large xerox / halftone block

### Meso — usually 2
Use supporting moves:
- one same-target portrait fragment
- tape
- red dry-brush gesture
- xerox patch
- chain / cross / safety-pin-like hardware
- medium halftone patch
- torn-paper overlap
- one graphic label

### Micro — usually 2–4
Use surface detail:
- scratches
- paper grain / fibers
- tiny X / star / heart / arrow
- ink speckle
- pencil / chalk residue
- small misregistration
- distressed print residue

If the image looks weak, strengthen Macro first.  
If it looks messy, remove Micro first.

## 9. Preset intensity

### Clean
- portrait attention: about 80–90%
- background transformation: light
- 1 macro move
- 1–2 meso moves
- sparse micro texture
- 0–1 portrait fragment
- generous negative space

### Editorial — default
- portrait attention: about 70–85%
- background transformation: clearly visible
- 1 dominant macro + optional counterweight
- about 2 meso moves
- controlled print texture
- 0–2 fragments, usually 0–1
- asymmetric zine hierarchy

### Chaotic
- portrait attention: about 60–80%
- background transformation: strong
- stronger macro collision
- 2–3 meso moves
- denser print / scratch / type energy
- 1–3 fragments maximum
- less negative space, but still one focal subject

Chaotic means stronger graphic density, not more duplicated faces.

## 10. Portrait fragments: same-target by default

Any added face, eye, mouth, hand, profile, or portrait crop must come from the TARGET image for that output.

For batch work:
- do not borrow a face or body part from another batch photo by default
- do not borrow from STYLE_REFERENCE images under any circumstance
- cross-photo portrait fragments are allowed only if the user explicitly requests them

If exact source reuse cannot be guaranteed, omit the portrait fragment and use non-portrait graphics instead.

Recommended limits:
- Clean: 0–1
- Editorial: 0–2, usually 0–1
- Chaotic: 1–3 maximum

## 11. Face and hand occlusion budget

Unless the user explicitly asks for obstruction:

- eyes, nose, mouth: no graphic occlusion
- defining face contour: keep readable
- fingers and hand silhouette: keep readable
- hair / shoulder / clothing edges: controlled overlap is allowed
- background immediately behind the subject: may be heavily redesigned

The strongest tears, type, or paint should usually collide with silhouette edges, not the center of the face.

## 12. Palette and material

Read references/style-guide.md.

Default graphic palette:
- black / charcoal: dominant
- deep red / oxblood / dark wine: accent
- dirty white / off-white / photocopy gray: contrast
- natural skin and meaningful source colors: preserved

Apply palette dominance mainly to the redesigned graphic/background regions.

Do not force the person into a palette percentage.

Avoid a global sepia / warm-brown cast unless requested.

## 13. Torn paper is structure, not decoration

At least one major tear or paper field must do compositional work by:

- entering the image interior
- separating photography from graphic space
- passing behind or around the person
- redirecting the eye
- creating a black / white division
- breaking the original photographic frame

Avoid equal torn borders on all four sides.

## 14. Typography and “no text”

If the user supplies exact text:
- reproduce it exactly
- preserve capitalization
- use the primary phrase once by default
- keep it away from defining facial features unless overlap is requested

If the user says **No text**:
- use no readable words
- use no letters unless the user explicitly asks for typographic texture

If the user says **No readable text**:
- no readable words or phrases
- abstract / cropped / damaged letterforms may be used sparingly only when they clearly function as texture

Do not invent slogans, magazine headlines, captions, or motivational English.

## 15. Batch / series planner

For two or more TARGET images, build an internal **Series Plan** before editing.

Lock across the batch:
- red hue
- black / off-white relationship
- paper family
- xerox / grain character
- contrast philosophy
- typography family
- overall mood

Vary across the batch:
- composition family
- subject placement
- tear direction
- red gesture direction
- negative-space amount
- fragment use / non-use
- typography scale and position
- halftone location
- crop intensity

Two adjacent outputs should not repeat the same macro geometry unless the user requests a deliberate pair.

## 16. Pixel-visible prompt compiler

Before calling the image editor, compile only instructions that can become visible pixels.

Use this order:

1. Identify the TARGET and state that STYLE_REFERENCE people are style-only and must not appear.
2. Lock identity, face, pose, hands, clothes, jewelry, angle, and orientation.
3. State which target regions should remain photographically faithful.
4. State the selected composition family.
5. State what happens to the original background.
6. State the dominant Macro move and optional counterweight.
7. State the Meso moves.
8. State the Micro texture budget.
9. State palette / material behavior.
10. State portrait-fragment rule: same TARGET only or none.
11. State exact text behavior.
12. State batch continuity if applicable.
13. State hard avoids.

Do not put hidden analysis, file paths, percentages-as-theory, or long design explanations into the generation prompt.

## 17. Generate, inspect, recover

After generation, inspect against references/quality-gate.md.

Regenerate once before presenting if any critical failure occurs, especially:

- identity drift
- changed pose / hand / clothing
- style-reference person or body part leaks into the result
- invented portrait fragment
- changed orientation
- random readable text
- border-only treatment
- original background still dominates in Editorial / Chaotic
- no internal graphic collision
- clutter with no hierarchy
- duplicated batch layout

Recovery sequence:

1. return to the original TARGET
2. remove optional portrait fragments
3. reduce one density level
4. keep one composition family only
5. restate the portrait lock and reference-contamination ban
6. regenerate once

If identity still drifts, simplify the background treatment rather than pushing style harder.

## 18. Output behavior

When editing tools are available:
- edit directly
- keep already-stated preferences across the batch
- do not ask the same setup questions for every image
- do not precede the edit with a long explanation
- show the image result first

Only provide rationale, prompt details, or composition notes when the user asks.

## 19. One-line definition

**Lock the real TARGET person, classify style references as style-only, choose one source-aware poster composition, rebuild the surrounding space with black / oxblood / dirty-white torn-paper and xerox structure, use only sparse same-target portrait fragments, and reject anything that reads as a border/filter treatment, reference-person contamination, or an AI look-alike.**
