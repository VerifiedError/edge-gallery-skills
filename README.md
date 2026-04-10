# edge-gallery-skills

Custom skills for the [Google AI Edge Gallery](https://github.com/google-ai-edge/gallery) Android app.

## How to import a skill

1. Open **AI Edge Gallery** on your phone
2. Start a chat with any model (Gemma 4, etc.)
3. Open **Skill Manager** (the **Skills** chip)
4. Tap **(+)** → **Load skill from URL**
5. Paste the skill's GitHub Pages folder URL (see below)

> Important: the URL must point to the **skill folder** (not the `SKILL.md` file itself).
> GitHub Pages is required — `raw.githubusercontent.com` won't work due to MIME types.

## Available skills

| Skill | Description | Import URL |
|---|---|---|
| `my-location` | Get current GPS coordinates + street address | `https://<user>.github.io/edge-gallery-skills/my-location/` |

## Publishing (one-time setup)

1. Push this repo to GitHub
2. Settings → Pages → Source: **Deploy from a branch** → `main` / `/ (root)`
3. Wait ~1 min for deployment
4. Verify: open `https://<user>.github.io/edge-gallery-skills/my-location/SKILL.md` in a browser — you should see the raw markdown.

The `.nojekyll` file at the repo root disables Jekyll processing so markdown files are served raw.
