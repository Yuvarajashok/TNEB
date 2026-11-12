# TNEB Bill Calculator

A small browser-based electricity-bill calculation project by Yuvaraj Ashok, implemented in one HTML file with embedded CSS and JavaScript.

## Open and use

1. Download or clone this repository.
2. Open [Yuvaraj_Project_TNEB.html](Yuvaraj_Project_TNEB.html) in a JavaScript-enabled browser.
3. Enter a non-negative whole number of consumed units using the keypad or text field.
4. Select **Calculate** to display the amount.
5. Select **C** before starting another calculation.

No Python, npm, database, server, or installation step is required by this file.

## What it contains

- Numeric keypad and editable input.
- Four calculation branches based on consumed units.
- Calculate and clear actions.
- HTML structure, inline CSS styling, and JavaScript functions `dis`, `solve`, and `clr`.

## Calculation scope

The rates are hardcoded in the source. Their tariff effective date, official source, consumer category, and billing period are not documented in the original project. This repository does **not** establish that these are current official tariffs. Treat the output as a demonstration of the implemented formula.

See [calculation rules, examples, and limitations](docs/CALCULATION.md).

## Project status

The documentation describes the checked-in source; browser compatibility and UI screenshots have not been validated in this documentation update. No screenshot or hosted demo is supplied.

## Contributions and licensing

See [CONTRIBUTING.md](CONTRIBUTING.md). No license file has been supplied by the owner; this documentation does not select or grant a new software license.
