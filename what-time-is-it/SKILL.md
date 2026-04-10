---
name: what-time-is-it
description: Get the current local time, date, day of the week, and timezone. Use when the user asks "what time is it", "what day is it", "what's the date", or wants to know the current time in a specific timezone.
metadata:
  homepage: https://github.com/addisonmikkelson/edge-gallery-skills
---

# Instructions

When the user asks about the current time or date, you MUST use the `run_js` tool with:

- script name: index.html
- data: A JSON string. Empty `{}` for the user's local time, or `{"timezone":"America/New_York"}` to convert to a specific IANA timezone.

## Result fields

- `result` — pre-formatted human-readable summary you can show directly
- `iso` — full ISO 8601 timestamp
- `local` — e.g. `"Thursday, April 9, 2026, 3:47 PM"`
- `day_of_week` — e.g. `"Thursday"`
- `date` — `"YYYY-MM-DD"`
- `time` — `"HH:MM:SS"` (24h)
- `timezone` — IANA name (e.g. `"America/Chicago"`)
- `offset` — e.g. `"UTC-05:00"`
- `is_dst` — `true`/`false` (best-effort)
- `error` — null on success

## Examples

- "What time is it?" → call with `{}`
- "What day is today?" → call with `{}`
- "What time is it in Tokyo?" → call with `{"timezone":"Asia/Tokyo"}`
