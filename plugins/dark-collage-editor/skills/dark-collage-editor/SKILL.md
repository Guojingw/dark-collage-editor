---
name: dark-collage-editor
description: Turn user-supplied portrait photos into a dark red-black-white collage/graffiti editorial style while preserving the person's identity, pose, orientation, and source-photo authenticity. Use for one photo or a batch when the user wants grunge, punk, goth, zine, torn-paper, graffiti, photocopy, or dark editorial portrait edits with optional custom text.
---

# Dark Collage Editor

Use this skill when a user wants portrait photos edited into a dark collage / graffiti / zine / punk / goth editorial style.

## Core promise

The edited result should still look like the user's original photograph and person, not a newly generated look-alike.

Hard rules:
- Preserve identity, face structure, hairstyle, body pose, clothing, accessories, camera angle, and image orientation unless the user explicitly asks to change them.
- Keep portrait fragments sparse. Default: 0–2 supporting photo fragments per image.
- Any face, eye, mouth, hand, or portrait fragment used in the collage must come from the user's uploaded source photos. Never invent an extra face or use an unrelated person.
- If the environment cannot make a true crop/reuse of the user's source photo, omit that portrait fragment instead of synthesizing one.
- Increasing “chaos” means adding more paper, graffiti, typography, scratches, tape, ink, halftone, and texture — not duplicating the person's face repeatedly.
- Never replace the main portrait with a newly imagined portrait.
- Do not alter horizontal photos into vertical photos or vertical photos into horizontal photos unless the user requests it.

## First-use flow: keep it simple

Do not make the user write prompts or choose technical settings.

If photos are not attached, ask the user to upload them.

When photos are attached and essential preferences are missing, ask at most three short questions:
1. Style strength: **Clean / Editorial / Chaotic**. Default: **Editorial**.
2. Text: ask for exact wording, or **No text**. Never invent main copy unless the user explicitly asks you to write it.
3. Batch behavior when there are multiple photos: **Consistent series / More variation**. Default: **Consistent series**.

If the user already supplied these preferences, start editing without asking again.

## Visual language

Use a controlled palette:
- black / charcoal
- deep red / oxblood
- off-white / dirty white
- natural skin tones may remain visible

Preferred design elements:
- torn paper and ripped edges
- photocopy / xerox texture
- halftone dots
- film grain
- rough paper texture
- paint strokes and splatter
- marker / pencil / chalk scribbles
- tape fragments
- scratches and scuffs
- chains, crosses, safety-pin-like hardware, stars, hearts, arrows, abstract marks
- distressed type and small editorial text blocks

Avoid:
- filling every empty area
- repeated full faces around the whole canvas
- random decorative elements that cover important facial features
- fake magazine text the user did not ask for
- changing the person's facial identity to fit the style
- over-brightening the portrait

## Composition

The main portrait must remain dominant.

Recommended visual weight:
- Clean: main portrait about 80–90% of attention; 0–1 small source-photo fragment.
- Editorial: main portrait about 70–85%; 1–2 small source-photo fragments.
- Chaotic: main portrait about 60–80%; 1–3 source-photo fragments maximum.

Use torn paper, red paint, text, texture, and graffiti to occupy the remaining visual space.

Do not use the same layout for every image in a batch. Keep the visual language consistent while varying:
- collage fragment location
- red paint direction
- typography placement
- paper tear direction
- negative space
- graffiti density

## Text rules

Use the user's exact wording for prominent text.

Default text treatments:
- distressed serif / blackletter fragment
- photocopied sans serif
- typewriter label
- rough marker handwriting
- stencil
- cut-paper lettering

Text must not cover eyes, nose, mouth, or other defining facial features unless the user explicitly requests a face-obscuring composition.

If the user says “no text”, do not add decorative pseudo-copy or fake readable words. Abstract marks and texture are fine.

## Editing workflow

For each source photo:
1. Identify the main person, their pose, face, hands, outfit, accessories, and original orientation.
2. Preserve the main photograph as the visual anchor.
3. Select a preset from `presets/` based on the user's choice.
4. Decide whether supporting portrait fragments are actually needed. Fewer is usually better.
5. When using a supporting portrait fragment, reuse a crop from one of the user's uploaded source images. Prefer crops that add a genuinely different visual detail, such as an eye, hand, profile, or alternate pose.
6. Build the rest of the visual complexity using non-portrait collage elements: paper, ink, tape, texture, type, scratches, halftone, chains, and graffiti.
7. Apply color treatment without destroying the original subject's skin texture and lighting.
8. Keep the subject brighter / clearer than the surrounding collage unless the user asks for a silhouette-like result.
9. Review against `references/QUALITY_CHECKLIST.md` before finalizing.

## Batch workflow

For 2 or more photos, first plan the set as a visual series.

Keep consistent across the set:
- palette
- grain family
- paper texture family
- red tone
- typography family
- contrast level
- overall editorial mood

Vary across the set:
- composition
- placement of collage fragments
- where the red accents appear
- amount of negative space
- text size and position
- graffiti marks

Do not produce the same poster template repeatedly.

## Source-photo authenticity

When a user says portrait fragments must be from the person themself, treat this as a hard requirement.

If you cannot verify that a fragment is a real crop from the supplied source material, remove the fragment and replace it with non-portrait design elements.

Never claim a generated face fragment is an original crop.

## Output behavior

When editing tools are available, produce the edited image(s) directly.

For a batch, preserve the original file order and orientation. If the environment returns images one at a time, continue through the batch without asking the user to repeat the same preferences.

Do not add a long explanation after each generated image. Let the user react to the visual result and refine it.

If image-editing capability is unavailable, say so clearly and provide a concise edit plan rather than pretending the images were edited.
