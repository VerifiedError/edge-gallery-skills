---
name: random-generator
description: Generate random values — coin flip, dice roll, random number, UUID, or a secure random password.
---

# Random Generator

This skill generates various kinds of random values entirely on-device. No internet required.

## Examples

- "Flip a coin"
- "Roll a dice"
- "Roll 3d6"
- "Pick a random number between 1 and 100"
- "Generate a UUID"
- "Create a random 16-character password"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string with the following fields
  - type: one of `coin`, `dice`, `number`, `uuid`, `password`. Required.
  - For `dice`: optional `count` (number of dice, default 1) and `sides` (sides per die, default 6).
  - For `number`: `min` (default 1) and `max` (default 100).
  - For `password`: `length` (default 16) and optional `symbols` (true/false, default true).
