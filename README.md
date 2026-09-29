# Dark Collage Editor

A no-prompt-writing, source-faithful dark collage portrait workflow for ChatGPT/Codex plugins.

**Goal:** let a user upload portrait photos, choose a simple intensity level, optionally provide exact text, and get a coherent dark red / black / off-white grunge collage series without turning the canvas into repeated AI-generated faces.

## What it does

- Preserves the uploaded subject as the visual anchor.
- Keeps the original image orientation unless the user asks to change it.
- Uses black / deep red / off-white, torn paper, xerox grain, halftone, scratches, tape, chains and graffiti.
- Uses 0–2 supporting portrait fragments by default.
- Requires portrait fragments to come from the user's uploaded photos; if true source reuse is not available, it should omit them rather than synthesize a look-alike.
- Supports exact user-supplied text or no text.
- Supports batch / series editing with a consistent visual language but varied composition.

## For normal users

Typical requests:

> Edit these photos with Dark Collage Editor. Editorial. Text: STAY IN THE NOISE.

> 把这 9 张修成一组暗黑拼贴涂鸦风，Editorial，不要文字。

The skill asks only for missing essentials; users do not need prompt-engineering syntax.

## Repository layout

```text
.agents/plugins/marketplace.json
plugins/
  dark-collage-editor/
    plugin.json
    skills/
      dark-collage-editor/
        SKILL.md
        presets/
        references/
        examples/
```

## Test locally from this GitHub repository

Current OpenAI plugin authoring docs support Git-backed/local marketplaces in the ChatGPT desktop app and Codex.

1. Install/open the ChatGPT desktop app and make sure Plugins are available on your account.
2. Add this repository as a plugin marketplace:

```bash
codex plugin marketplace add Guojingw/dark-collage-editor
```

3. Restart the ChatGPT desktop app.
4. Open **Plugins** and choose the `Guojingw Creative Plugins` marketplace/source.
5. Install **Dark Collage Editor**.
6. Start a new chat, upload a portrait, and try:

> Use Dark Collage Editor. Editorial. No text. Preserve my face and pose.

Availability varies by ChatGPT plan, surface, and rollout. Personal raw Skills are generally limited to eligible Business / Enterprise / Healthcare / Edu accounts; plugins have broader availability, so this repository is packaged as a skills-only plugin for testing/distribution.

## Direct Skill upload

If your ChatGPT workspace has personal Skills upload enabled, upload the folder at:

```text
plugins/dark-collage-editor/skills/dark-collage-editor/
```

or zip that single top-level skill folder.

## Status

v0.2.0 — instruction-first prototype. The next substantial milestone is a deterministic source-crop/compositing engine so face/eye/hand collage fragments can be guaranteed pixel-for-pixel to originate from the uploaded source rather than relying only on model compliance.

## License

MIT. See `LICENSE`.
