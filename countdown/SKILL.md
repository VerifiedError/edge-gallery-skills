---
name: countdown
description: Count down to (or up from) any date or event and report days, hours, and minutes remaining.
---

# Countdown

This skill calculates exactly how much time remains until a future date, or how long it has been since a past date. No internet required.

## Examples

- "How many days until Christmas?"
- "How long until New Year's Eve?"
- "How many days since my birthday on March 15?"
- "Days until July 4th"
- "How long until 2027-01-01?"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string with the following fields
  - date: the target date as an ISO 8601 string (`YYYY-MM-DD` or `YYYY-MM-DDTHH:MM:SS`). Required.
  - label: optional short event name shown in the result (e.g. "Christmas", "New Year").

If the user mentions a well-known holiday by name, resolve it to the next upcoming occurrence of that date in the current or next year, then pass the ISO date.
