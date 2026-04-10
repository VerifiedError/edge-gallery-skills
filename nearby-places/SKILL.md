---
name: nearby-places
description: Find places near the user's current location — coffee shops, ATMs, restaurants, gas stations, pharmacies, banks, grocery stores, hotels, hospitals, parks. Use when the user asks "coffee near me", "nearest ATM", "where can I get food", etc. Uses OpenStreetMap data (no API key).
metadata:
  homepage: https://github.com/addisonmikkelson/edge-gallery-skills
---

# Instructions

When the user asks for nearby places, you MUST use the `run_js` tool with:

- script name: index.html
- data: A JSON string with:
  - `type` (required) — one of the supported types below
  - `radius_m` (optional) — search radius in meters, default `1500`, max `5000`
  - `limit` (optional) — max results, default `8`

## Supported types

| User says | `type` value |
|---|---|
| coffee, cafe, espresso | `cafe` |
| atm, cash machine | `atm` |
| restaurant, food, dinner | `restaurant` |
| fast food, burger | `fast_food` |
| gas, fuel, gas station | `fuel` |
| pharmacy, drugstore | `pharmacy` |
| bank | `bank` |
| grocery, supermarket | `supermarket` |
| hotel, lodging | `hotel` |
| hospital, ER | `hospital` |
| park | `park` |

Pick the closest match. If the user asks for something not in the list, use the closest category or set `type` to a valid OSM `amenity` or `shop` tag value.

## Result fields

- `result` — pre-formatted numbered list you can show directly
- `origin` — `{lat, lon}` the search was centered on
- `type` — the type searched
- `count` — number of results returned
- `places` — array of `{name, distance_m, address, lat, lon, tags}`
- `error` — null on success

## Presenting the result

Show the numbered list from `result` directly. Mention how far each place is. If `count` is 0, suggest increasing the radius.
