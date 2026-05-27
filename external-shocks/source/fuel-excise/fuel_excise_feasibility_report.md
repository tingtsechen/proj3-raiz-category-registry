# Fuel Excise Feasibility Report

Generated: 2026-05-21 00:05:08
Runtime seconds: 71.9

## Exposure Cohort Support

- High exposure users (top 20% positive fuel share): 39,331
- Low positive fuel users: 98,327
- Zero pre-fuel users: 44,734
- Positive-fuel q80 threshold: 4.37%
- Positive-fuel q90 threshold: 6.67%

## Clean Fuel Label Support

| Fuel label | Users | Txns | Sales | Median txn | P99 txn |
|---|---:|---:|---:|---:|---:|
| `auto_fuel_bp` | 196,107 | 2,032,467 | $114,671,833 | $30.01 | $203.08 |
| `grocery_fuel_attached` | 201,129 | 2,077,045 | $78,251,747 | $22.47 | $160.00 |
| `auto_fuel_ampol` | 173,912 | 1,465,934 | $76,672,471 | $29.36 | $183.86 |
| `auto_fuel_7eleven` | 171,254 | 2,240,624 | $67,999,233 | $13.24 | $146.59 |
| `auto_fuel_united_metro_mobil` | 97,604 | 627,700 | $27,779,131 | $30.20 | $170.00 |
| `auto_fuel_caltex` | 102,046 | 509,995 | $22,709,921 | $30.01 | $186.00 |
| `auto_fuel_shell` | 98 | 194 | $111,673 | $79.77 | $11,829.52 |
| `auto_fuel_coles_express` | 1,080 | 1,290 | $54,201 | $26.05 | $170.15 |
| `auto_fuel_woolworths_petrol` | 7 | 8 | $876 | $98.00 | $186.33 |

## High-Exposure Top-10 Contrast

Cut starts, 12-week window:
- Fuel share: 11.09% -> 7.48% (-3.61% points).
- Any-fuel rate: 75.79% -> 69.41%.
- Fuel count per active user: 2.254 -> 1.997.

Restoration, 12-week window:
- Fuel share: 5.55% -> 3.81% (-1.73% points).
- Any-fuel rate: 65.87% -> 65.09%.
- Fuel count per active user: 1.852 -> 1.848.

## Feasibility Verdict

- Use this report only as a support audit, not as a causal estimate.
- Proceed if high and comparison cohorts are large enough and the cut/restoration movement is interpretable.
- Next build should add user-week fixed-effect regressions and pre-trend/event-study plots.

## Output Files

- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/fuel_label_support.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/pre_fuel_exposure_summary.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/cohort_week_summary.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/cut_restore_contrast.csv`
