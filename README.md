# Dark Collage Editor

A no-code ChatGPT Project workflow for turning portrait photos into a dark red / black / off-white collage, graffiti, zine, punk, or goth editorial style.

The project is designed for people who do **not** want to install a Skill, use Codex CLI, write prompts, or run code.

## What users do

1. Open a ChatGPT Project configured with this repository's instructions.
2. Upload one or more portrait photos.
3. Say something simple such as:

> Editorial. No text. Keep my face, pose, clothing and original orientation.

or:

> Editorial. Text: STAY IN THE NOISE. Make these 8 photos one consistent series, but vary each layout.

## Core design principle

The original portrait remains the hero. Collage complexity should come mostly from torn paper, paint, typography, scratches, tape, halftone, grain and graffiti — not from filling the canvas with repeated copies of the person's face.

## Start here

Read **[START_HERE.md](START_HERE.md)**.

To make your own no-code ChatGPT Project, you only need:

- **[PROJECT_INSTRUCTIONS.md](PROJECT_INSTRUCTIONS.md)** → paste into Project Instructions
- **[STYLE_GUIDE.md](STYLE_GUIDE.md)** → upload as a Project file
- **3–6 reference images you are allowed to use publicly or privately** → optional but recommended

Then use **[TEST_CASES.md](TEST_CASES.md)** for a first smoke test.

## Repository structure

```text
dark-collage-editor/
├── README.md
├── START_HERE.md
├── PROJECT_INSTRUCTIONS.md
├── STYLE_GUIDE.md
├── TEST_CASES.md
├── CHANGELOG.md
├── LICENSE
└── examples/
    └── README.md
```

The earlier Skill / Plugin prototype remains available in Git history. The current main branch is intentionally Project-first and no-code.

## Status

Current direction: **Project-first beta**.

The workflow is instruction-based. It strongly requests source-faithful portrait preservation, but exact pixel-level reuse of face/eye/hand fragments is not yet enforced by a deterministic crop engine.

## License

MIT.
