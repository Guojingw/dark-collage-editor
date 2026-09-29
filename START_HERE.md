# Start Here — 5 Minute No-Code Setup

This is the recommended way to test Dark Collage Editor yourself from scratch.

You do **not** need:
- Codex CLI
- a Plugin
- a Skill installation
- Node.js
- Python
- an API key

## 1. Create a new ChatGPT Project

Create a new Project named:

**Dark Collage Editor — Beta**

Use a fresh Project so you can test the experience exactly like a new user.

## 2. Add the Project Instructions

Open **PROJECT_INSTRUCTIONS.md** in this repository.

Copy the complete contents into the Project's instruction field.

Do not rewrite or shorten it for the first test.

## 3. Upload the style guide

Upload **STYLE_GUIDE.md** as a Project file.

This gives the Project a separate visual reference document rather than mixing all style rules into the instruction field.

## 4. Optional: add 3–6 reference images

You can test without reference images first.

For a stronger style lock, add 3–6 examples that you have permission to use.

A useful reference set should contain different compositions:
- one Clean image
- two Editorial images
- one horizontal image
- one image with text
- one image with no text

Do not upload private CR2 originals to a public repository.

See **examples/README.md** for guidance.

## 5. Start a new chat inside the Project

Upload one portrait and send exactly:

> Editorial. No text. Preserve my face, pose, clothes and original orientation.

Check the output against Test 01 in **TEST_CASES.md**.

## 6. Test exact text

In a new turn, use another portrait and say:

> Editorial. Text: STAY IN THE NOISE. Use it once. Do not cover my face.

Check the output against Test 02.

## 7. Test a batch

Upload 4–9 photos and say:

> Make these one consistent dark collage series. Editorial. No text. Keep the same palette and texture family, but make every layout different. Do not create chaos by repeating my face.

Check the output against Test 03.

## What counts as a successful first test?

A good result should satisfy most of these:
- the person still looks like the source person
- the original pose is preserved
- horizontal stays horizontal and vertical stays vertical
- the main portrait remains dominant
- no wall of repeated faces
- no invented readable text when "No text" was requested
- custom text is spelled exactly
- a batch looks related but not template-copied

## If the result is wrong

Do not immediately rewrite the whole project.

Record which rule failed, for example:
- identity drift
- too many portrait fragments
- invented text
- composition too busy
- batch layouts too repetitive

Then update only the relevant section of PROJECT_INSTRUCTIONS.md or STYLE_GUIDE.md and re-run the same test case.

This repository is meant to make iteration measurable rather than turning every failure into a new giant prompt.
