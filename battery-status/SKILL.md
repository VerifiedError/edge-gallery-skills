---
name: battery-status
description: Get the phone's current battery level and charging state. Use when the user asks "what's my battery", "how much battery do I have", "am I charging", "how long until full", "how long will my battery last", etc.
metadata:
  homepage: https://github.com/addisonmikkelson/edge-gallery-skills
---

# Instructions

When the user asks about battery, you MUST use the `run_js` tool with:

- script name: index.html
- data: An empty JSON string `{}`

## Result fields

- `result` — pre-formatted summary you can show directly
- `level_pct` — integer 0–100
- `charging` — `true`/`false`
- `charging_time_min` — minutes until full (or `null`)
- `discharging_time_min` — minutes until empty (or `null`)
- `error` — null on success

## Presenting the result

Show the percentage, charging state, and — if available — the estimated time to full or empty. Example: *"Battery 67%, not charging, ~4h 12m remaining."*

If `error` is not null, the Battery Status API may be unavailable in this WebView (some Android builds disable it for privacy). Tell the user honestly.
