---
name: my-location
description: Get the user's current physical location at any time. Returns GPS coordinates and the nearest street address. Use whenever the user asks "where am I", "what's my location", "get my current location", "where is my phone", or anything similar.
metadata:
  homepage: https://github.com/addisonmikkelson/edge-gallery-skills
---

# Instructions

When the user asks for their current location, you MUST use the `run_js` tool with the following exact parameters:

- script name: index.html
- data: An empty JSON string `{}` (no parameters required)

## Presenting the result

The script returns a JSON string with these fields:

- `result` — a pre-formatted human-readable string you can show directly
- `source` — either `gps` (precise) or `ip` (approximate, city-level)
- `latitude`, `longitude` — decimal degrees
- `accuracy_m` — accuracy radius in meters (GPS only)
- `address` — reverse-geocoded street address (best-effort, may be null)
- `city`, `region`, `country` — parsed components
- `error` — null on success, or an error message on failure

Present the location to the user in a friendly, scannable way. Always include:

1. The street address or city if available
2. Latitude and longitude
3. Whether the reading is precise (GPS) or approximate (IP-based)
4. Accuracy in meters when available

If `error` is not null, explain what went wrong and remind the user they may need to grant location permission to the Google AI Edge Gallery app in Android Settings → Apps → AI Edge Gallery → Permissions → Location.

## Examples of when to use this skill

- "Where am I?"
- "What's my current location?"
- "Get my GPS coordinates"
- "Find where I am right now"
- "What city am I in?"
