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
| `my-location` | Current GPS coordinates + reverse-geocoded street address | `.../my-location/` |
| `what-time-is-it` | Current local time, date, day of week, optional timezone conversion | `.../what-time-is-it/` |
| `battery-status` | Phone battery level, charging state, time to full/empty | `.../battery-status/` |
| `nearby-places` | Coffee, ATMs, gas, food, etc. near you (OpenStreetMap, no API key) | `.../nearby-places/` |
| `weather-here` | Current weather at your location (Open-Meteo, no API key) | `.../weather-here/` |
| `qr-wifi` | Generate a QR code to auto-join a Wi-Fi network | `.../qr-wifi/` |

Full import URL = `https://<your-username>.github.io/edge-gallery-skills/<skill-name>/`

## Publishing (one-time setup)

1. Push this repo to GitHub
2. Settings → Pages → Source: **Deploy from a branch** → `main` / `/ (root)`
3. Wait ~1 min for deployment
4. Verify: open `https://<user>.github.io/edge-gallery-skills/my-location/SKILL.md` in a browser — you should see the raw markdown.

The `.nojekyll` file at the repo root disables Jekyll processing so markdown files are served raw.
