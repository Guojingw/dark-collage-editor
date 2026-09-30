# Quality Gate — Dark Collage Editor v2

Inspect every generated result before presenting it.

## Critical failures — regenerate once

Regenerate if any of these occur:

### Identity
- face no longer looks like the supplied person
- defining facial proportions changed
- hairstyle changed materially
- expression changed without request
- pose changed
- hands were rebuilt incorrectly
- clothing or jewelry changed
- camera angle changed
- horizontal / vertical orientation changed

### Source authenticity
- an added eye, mouth, face, hand, or portrait fragment cannot be verified as source-derived
- an unrelated person appears
- duplicated face spam appears

### Text
When the user requested no readable text:
- a readable slogan, headline, caption, fake magazine copy, or random sentence appears

When exact text was supplied:
- spelling / capitalization is wrong
- main phrase appears repeatedly without request

### Composition
- result is mostly source photo with a decorative border
- torn paper exists only at the edges
- Editorial / Chaotic leaves the original background visually dominant
- no large graphic structure enters the image interior
- all visual elements have equal weight
- collage hides the main person
- red is sprayed evenly with no compositional function

### Batch
- same layout is copied across multiple images
- same portrait fragment placement repeats mechanically
- every image has the same red block and tear direction
- series palette or material language drifts unintentionally

## Secondary failures — simplify or correct

- too many small marks
- too many hardware motifs
- too much halftone on the face
- black crush removes clothing detail
- red contaminates skin
- no negative space
- macro structure too weak
- typography too busy
- torn-paper edge looks like a clean sticker outline
- warm brown / sepia dominates unintentionally

## Pass criteria

A successful result should satisfy most of these:

- same person at first glance
- same pose and orientation
- face remains the clearest identity anchor
- source background is meaningfully redesigned when appropriate
- one clear macro composition is visible
- black / deep red / dirty white relationship feels intentional
- torn paper participates in the image interior
- portrait fragments are sparse and source-authentic
- texture supports rather than replaces composition
- no unwanted readable text
- batch feels related but not templated

## Recovery strategy

If the first generation fails:

1. keep the original source image
2. reduce collage density by one level
3. simplify to one composition family
4. remove optional portrait fragments
5. restate face / hands / clothes / pose as locked
6. regenerate once

If identity still drifts, choose a simpler family such as Split Photography or Graphic Negative Space instead of forcing a stronger cutout transformation.
