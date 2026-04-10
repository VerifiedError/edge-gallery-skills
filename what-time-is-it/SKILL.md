---
name: what-time-is-it
description: Get the current local time, date, day of the week, and timezone.
---

# What Time Is It

This skill returns the current local time and date, including the day of the week and timezone. Optionally converts to a different IANA timezone.

## Examples

- "What time is it?"
- "What day is today?"
- "What's the date?"
- "What time is it in Tokyo?"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string with optional fields
  - timezone: an IANA timezone name like `America/New_York` or `Asia/Tokyo`. Omit for the user's local time.
