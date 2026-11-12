# Calculation reference

[Back to README](../README.md)

## Source behavior

The `solve()` function in [the HTML file](../Yuvaraj_Project_TNEB.html) applies `parseInt` to the text field and selects one branch. The table below transcribes the code; it is not an official tariff schedule.

| Parsed units u | Displayed amount calculation |
| --- | --- |
| 0 through 100 | Text: Free |
| More than 100 through 200 | (u - 100) × 1.5 + 20 |
| More than 200 through 500 | (u - 200) × 3 + 200 + 30 |
| Otherwise | (u - 500) × 6.6 + 100 × 3.5 + 300 × 4.6 + 50 |

The last branch also receives invalid or negative input because there is no separate validation branch. Only non-negative whole-number examples are meaningful for the intended use.

## Worked examples

These are arithmetic expectations derived from the source, not recorded browser test results.

| Input | Expected amount |
| --- | --- |
| 0 | Free |
| 100 | Free |
| 101 | 21.5 |
| 150 | 95 |
| 200 | 170 |
| 201 | 233 |
| 500 | 1130 |
| 501 | 1786.6 |
| 600 | 2440 |

For 150 units: (150 - 100) × 1.5 + 20 = 95.

The jumps between 100/101, 200/201, and 500/501 follow the current code. They have not been reconciled with an official tariff.

## Limits and troubleshooting

- A decimal keypad button exists, but `parseInt` discards the fractional part. Use whole units.
- Blank input, negative numbers, or arbitrary text are not validated; results can be misleading or NaN.
- Calculate replaces the input with `Amount : ...`. Press **C** before a new calculation.
- Currency rounding is not explicitly implemented.
- No consumer category, billing-period selector, or tariff-date selector exists.
- If buttons do nothing, check that JavaScript is enabled and that the downloaded file is opened as HTML.
- Mobile layout and browser compatibility have not been tested for this documentation change.

## Information needed to verify the tariff

Record the official tariff document, effective dates, billing period, consumer category, and treatment of subsidies/fixed charges before presenting this as a real billing calculator. None of these details is inferred here.

## Suggested manual check

Open the file, try the boundary examples above, verify **C** resets the display, and inspect the layout at desktop and phone widths. Record the browser/version and actual results. A screenshot should be captured from the real application after this check; no fabricated preview is included.
