---
name: battery-status
description: Get the phone's current battery level and charging state.
---

# Battery Status

This skill reports the phone's battery level, whether it's charging, and an estimate of time to full or empty when available.

## Examples

- "What's my battery?"
- "How much battery do I have?"
- "Am I charging?"
- "How long until my phone is full?"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string. Pass `{}`.
