---
name: qr-wifi
description: Generate a QR code that, when scanned by a phone camera, auto-joins a Wi-Fi network. Use when the user says "make a QR code for my Wi-Fi", "share my Wi-Fi", "QR code to join the network", etc.
metadata:
  homepage: https://github.com/addisonmikkelson/edge-gallery-skills
---

# Instructions

When the user wants a Wi-Fi QR code, you MUST use the `run_js` tool with:

- script name: index.html
- data: A JSON string with:
  - `ssid` (required) — the network name
  - `password` (optional) — network password; omit for open networks
  - `security` (optional) — `"WPA"` (default), `"WEP"`, or `"nopass"`
  - `hidden` (optional) — `true` if the SSID is hidden; default `false`

If the user hasn't given you a password, ask for it before calling the tool (unless they say it's an open network).

## Result fields

- `result` — a short success message you can show
- `image` — `{ base64: "<PNG base64>", mime: "image/png" }` — the QR code
- `payload` — the raw Wi-Fi string encoded in the QR (for debugging)
- `error` — null on success

## Presenting the result

The `image` field is rendered directly by Edge Gallery — you don't need to describe the QR visually. Just confirm it was generated and tell the user to scan it with their camera app.

**Security note:** A Wi-Fi QR code embeds the password in plain text. Warn the user not to share the QR publicly if the network is sensitive.
