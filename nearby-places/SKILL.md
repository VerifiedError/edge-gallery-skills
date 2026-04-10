---
name: nearby-places
description: Find places near the user's current location like coffee shops, ATMs, restaurants, gas stations, pharmacies, banks, grocery stores, hotels, hospitals, and parks.
---

# Nearby Places

This skill finds places of a given type near the user's current location using OpenStreetMap data. No API key required.

## Examples

- "Coffee shops near me"
- "Find the nearest ATM"
- "Where's the closest gas station?"
- "Show me pharmacies nearby"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string with the following fields
  - type: one of `cafe`, `atm`, `restaurant`, `fast_food`, `fuel`, `pharmacy`, `bank`, `supermarket`, `hotel`, `hospital`, `park`. Pick the closest match to what the user asked for.
  - radius_m: optional search radius in meters, default 1500, max 5000.
