# Dark Collage Editor — Smoke Tests

Run these after creating a fresh ChatGPT Project.

The goal is to test the workflow as a normal user would experience it.

---

## Test 01 — Single image, no text

### Input
One portrait.

### User message

> Editorial. No text. Preserve my face, pose, clothes and original orientation.

### Pass criteria
- identity remains recognizably the same
- pose remains the same
- clothing and accessories are not redesigned
- horizontal / vertical orientation is preserved
- one dominant portrait remains the focus
- no invented readable phrase appears
- no more than two supporting portrait fragments
- visual density comes mostly from paper / paint / grain / graffiti

---

## Test 02 — Exact custom text

### Input
One portrait.

### User message

> Editorial. Text: STAY IN THE NOISE. Use it once. Do not cover my face.

### Pass criteria
- text is spelled exactly **STAY IN THE NOISE**
- it appears once as the main readable phrase
- it does not cover defining facial features
- identity and pose remain stable
- design still feels photographic rather than fully regenerated

---

## Test 03 — Batch / series

### Input
4–9 portraits.

### User message

> Make these one consistent dark collage series. Editorial. No text. Keep the same palette and texture family, but make every layout different. Do not create chaos by repeating my face.

### Pass criteria
- all images share black / deep-red / off-white language
- grain and paper families feel related
- each layout is visibly different
- repeated faces do not become the main method of variation
- original orientation is preserved per image
- no invented readable copy
- the set feels like one editorial series

---

## Test 04 — Chaotic without face spam

### Input
One portrait.

### User message

> Chaotic. No text. Make it aggressive with torn paper, red paint, scratches and graffiti. Do not add extra repeated faces.

### Pass criteria
- higher design density than Editorial
- no wall of faces
- main person remains readable
- increased chaos comes from non-portrait graphics

---

## Test 05 — Minimal user request

### Input
One portrait.

### User message

> Make this dark collage style.

### Expected behavior
The Project should either:
- use defaults: Editorial + No text, or
- ask only the short missing preference questions defined in PROJECT_INSTRUCTIONS.md

It should not ask for technical parameters or make the user write a long prompt.

---

## Failure log template

When a test fails, record only the failure category and evidence.

```text
Test:
Source:
Failure category:
- identity drift
- pose drift
- orientation changed
- too many portrait fragments
- invented text
- text misspelled
- too cluttered
- batch layouts too repetitive
- style too weak
- other

Observed:
Expected:
Next rule to adjust:
```

Keep the same source image and test prompt when comparing instruction revisions.
