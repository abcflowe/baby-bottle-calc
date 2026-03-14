# Baby Bottle Formula Calculator

A mobile-friendly single-page calculator for preparing baby formula bottles.

## Modes

### Scoop Mode
Rounds up to whole scoops. Shows total scoops needed, oz of water, and any extra formula produced.

### Scale Mode
Calculates exact grams of powder per bottle — no rounding. Shows per-bottle breakdown with grams of powder and oz of water for precise preparation using a kitchen scale.

## Measurement Constants

| Measurement                | Value   |
|----------------------------|---------|
| Water per scoop            | 2 oz    |
| Powder per scoop (volume)  | 0.2 oz  |
| Total formula per scoop    | 2.2 oz  |
| Powder per scoop (weight)  | 8.6 g   |

## Formulas

Given a desired bottle size of **X oz** (total):

- **Scoops needed** = X / 2.2
- **Water (oz)** = scoops × 2
- **Powder (grams)** = scoops × 8.6
- **Powder (oz)** = scoops × 0.2

### Scoop mode rounding
Scoops are rounded **up** (ceiling) to the nearest whole scoop. This means:
- Total made = ceil(X / 2.2) × 2.2
- Extra = total made − X

### Scale mode (exact)
No rounding — fractional scoops are converted directly to grams for weighing.

## Features
- Toggle between Scoop and Scale modes (persisted in localStorage)
- Add multiple bottles
- Bottle values persist across sessions via localStorage
- Decimal input supported
