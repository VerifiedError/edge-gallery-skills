---
name: weather-here
description: Get the current weather at the user's location including temperature, conditions, humidity, wind, and today's forecast.
---

# Weather Here

This skill returns the current weather at the user's location using Open-Meteo. No API key required.

## Examples

- "What's the weather?"
- "Is it raining?"
- "How hot is it outside?"
- "What's the weather today in Celsius?"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string with optional fields
  - units: either `imperial` (default, Fahrenheit and mph) or `metric` (Celsius and km/h).
