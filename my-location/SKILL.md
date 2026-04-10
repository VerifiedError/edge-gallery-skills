---
name: my-location
description: Get the user's current physical location (GPS coordinates and nearest street address).
---

# My Location

This skill returns the user's current geographic location. It uses the phone's GPS when available and falls back to an IP-based lookup when it isn't.

## Examples

- "Where am I?"
- "What's my current location?"
- "Get my GPS coordinates"
- "What city am I in?"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string. Pass `{}`.
