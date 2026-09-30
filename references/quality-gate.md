# Quality Gate — Dark Collage Editor v3

Inspect every generated image before presenting it. The purpose is to catch identity drift, style-reference contamination, weak collage structure, and batch repetition.

## A. Critical failures — regenerate once

### 1. Portrait fidelity
Regenerate if:
- the face no longer looks like the TARGET
- facial proportions or defining features changed
- hairstyle / hairline changed materially
- expression changed without request
- pose or camera angle changed
- hands or finger count were rebuilt incorrectly
- clothes, jewelry, accessories, tattoos, piercings, or makeup changed
- original horizontal / vertical orientation changed

### 2. Style-reference contamination
Regenerate if any person-derived content from a STYLE_REFERENCE appears in the result:
- another face
- another eye
- another hand
- another hairstyle
- another outfit
- another body or pose
- a portrait fragment that cannot be traced to the TARGET

Style references may influence visual language only.

### 3. Fragment authenticity
Regenerate if:
- an added portrait fragment is invented
- a fragment comes from another batch photo without explicit permission
- a fragment is source-ambiguous
- face duplication becomes the main source of “chaos”

When uncertain, remove the fragment.

### 4. Text
If the user requested No text:
- any readable word or visible letterform is a failure unless explicitly allowed later

If the user requested No readable text:
- a readable slogan, headline, caption, or phrase is a failure

If exact text was supplied:
- spelling, capitalization, wording, or repeated placement is wrong

### 5. Composition
Regenerate if:
- result is mostly the original photo with an outer border
- torn paper exists only around the perimeter
- no large graphic structure enters the image interior
- Editorial / Chaotic leaves the original background visually dominant without a source-based reason
- every element has equal visual weight
- the collage hides the main person
- red is scattered evenly without a compositional role
- the result looks like stickers pasted around a photo rather than one integrated poster

### 6. Batch
Regenerate the affected page if:
- the same composition family repeats mechanically
- tear direction, red block, fragment placement, and subject placement all repeat
- the page is nearly a template duplicate
- palette / paper / xerox language drifts unintentionally
- the batch loses per-image orientation

## B. Secondary failures — simplify before regenerating

Correct or simplify if:
- too many small marks
- too many hardware motifs
- too much halftone over the face
- black crush destroys clothing detail
- red contaminates skin
- there is no quiet area
- macro structure is too weak
- typography is too busy
- torn paper looks like a clean sticker outline
- warm brown / sepia dominates unintentionally
- the style reference is being copied too literally
- the page contains more visual ideas than can be read at thumbnail size

## C. Four fast visual tests

### Thumbnail test
At small size the image should read:
1. person
2. one large graphic idea
3. black / oxblood / dirty-white relationship
4. texture

If tiny scratches or symbols read first, simplify.

### Identity test
Compare directly with the TARGET:
- same face
- same pose
- same hands
- same clothes
- same jewelry
- same orientation

### Interior-collision test
At least one major tear, type field, black/white block, halftone field, or red structure must participate inside the composition, not only around the border.

### Reference-contamination test
Mentally remove all style references. Every human feature in the result must still be explainable from the TARGET alone.

## D. Pass criteria

A strong result should satisfy all critical and most secondary criteria:

- same person at first glance
- same pose and orientation
- face remains the identity anchor
- background is meaningfully redesigned when preset calls for it
- one clear macro composition exists
- black / oxblood / dirty-white relationship is intentional
- torn paper participates in the interior
- portrait fragments are sparse and same-target
- red has a job
- texture supports composition
- no unwanted readable text
- style reference affects language, not content
- batch feels coherent but not templated

## E. Recovery strategy

If first generation fails:

1. return to the original TARGET
2. explicitly restate that all STYLE_REFERENCE people are forbidden content donors
3. remove optional portrait fragments
4. reduce density one level
5. keep one composition family and one Macro move
6. protect face / hands / clothes / jewelry / pose again
7. regenerate once

If identity still drifts:
- use Split Photography or Graphic Negative Space
- keep more of the original portrait field intact
- simplify graphic overlap
- do not compensate by adding more generated detail

If style is too weak but identity is correct:
- strengthen the Macro field or tear
- increase background replacement
- do not increase Micro clutter first
