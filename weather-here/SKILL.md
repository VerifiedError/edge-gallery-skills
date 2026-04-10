---
name: weather-here
description: Get current weather at the user's location — temperature, conditions, humidity, wind, and a short forecast for the rest of the day. Uses Open-Meteo (no API key). Temperatures returned in Fahrenheit by default. Use when the user asks "what's the weather", "is it raining", "how hot is it", "weather today".
metadata:
  homepage: https://github.com/addisonmikkelson/edge-gallery-skills
---

# Instructions

When the user asks about the weather, you MUST use the `run_js` tool with:

- script name: index.html
- data: A JSON string. Empty `{}` for Fahrenheit, or `{"units":"metric"}` for Celsius.

## Result fields

- `result` — pre-formatted summary you can show directly
- `temperature` — current temp (°F or °C)
- `feels_like` — apparent temperature
- `conditions` — text description (e.g. "Partly cloudy")
- `humidity_pct` — relative humidity
- `wind_speed` — mph or km/h
- `wind_dir` — cardinal direction (N, NE, E, etc.)
- `precipitation` — current precip amount
- `today_high`, `today_low` — daily forecast
- `location_label` — nearest city, if known
- `units` — `"imperial"` or `"metric"`
- `error` — null on success

## Presenting the result

Show the summary plainly. Lead with temperature and conditions, then add humidity/wind as a second line.
