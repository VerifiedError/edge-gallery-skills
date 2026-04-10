---
name: unit-converter
description: Convert between common units of length, weight, temperature, volume, area, and speed.
---

# Unit Converter

This skill converts a value from one unit to another. Supports length, weight, temperature, volume, area, and speed. No internet connection required.

## Examples

- "Convert 5 miles to kilometers"
- "How many pounds is 70 kg?"
- "Convert 100 Fahrenheit to Celsius"
- "How many liters is 2 gallons?"
- "Convert 60 mph to km/h"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string with the following fields
  - value: the numeric value to convert. Required.
  - from: the source unit (see list below). Required.
  - to: the target unit (see list below). Required.

Supported units (use lowercase):

- **Length**: `m`, `km`, `cm`, `mm`, `ft`, `in`, `yd`, `mi`, `nmi`
- **Weight / Mass**: `kg`, `g`, `mg`, `lb`, `oz`, `st`, `t`
- **Temperature**: `c`, `f`, `k`
- **Volume**: `l`, `ml`, `cl`, `m3`, `gal`, `qt`, `pt`, `cup`, `floz`, `tsp`, `tbsp`
- **Area**: `m2`, `km2`, `cm2`, `ft2`, `in2`, `acre`, `ha`
- **Speed**: `mps`, `kph`, `mph`, `knot`, `fps`

If the user writes units in a natural way (e.g. "miles", "kilograms", "gallons"), map them to the abbreviations above before calling the tool.
