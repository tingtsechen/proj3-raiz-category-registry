# Fuel Excise Exposure Outcome Audit

Generated: 2026-05-27 12:15:37
Runtime seconds: 540.7

## What This Adds

This audit keeps the existing pre-shock fuel-intensity cohorts and asks whether high-fuel users move differently from low-positive-fuel users around the national fuel excise cut and restoration.

Important: this is still descriptive. High-fuel users are not randomly assigned, so the high-minus-low columns are a screening contrast, not a causal estimate.

## Cohort Definition

- Pre-period: `2022-01-03` to `2022-03-28` exclusive.
- Cut date: `2022-03-30`; restoration date: `2022-09-29`.
- Positive-fuel q80 threshold: 4.37%.
- Positive-fuel q90 threshold: 6.67%.

## Outcome Families

| Outcome | Family | Definition |
|---|---|---|
| `direct_fuel` | mobility | Rows matching clean fuel labels from the existing fuel-excise feasibility audit. |
| `gambling_total` | risky_finance_adjacent | semantic_subcat_v2 begins with gambling_. |
| `gambling_lottery` | risky_finance_adjacent | semantic_subcat_v2 = gambling_lottery. |
| `bnpl_total` | finance_adjacent_credit | semantic_subcat_v2 in Afterpay/Zip/Klarna/Humm/Openpay/Laybuy/LatitudePay labels. |
| `insurance_total` | finance_adjacent_risk | clean_category = Insurance or semantic_subcat_v2 begins with insurance_. |
| `grocery_ex_fuel` | essentials | clean_category = Groceries excluding clean fuel labels. |
| `home_improvement` | durable_home | clean_category = Home Improvement. |
| `healthcare_total` | essentials | clean_category = Healthcare & Medical or pharmacy-style semantic labels. |
| `entertainment_ex_gambling` | hedonic | clean_category = Entertainment & Recreation excluding gambling labels. |
| `travel_total` | reopening_sensitive | clean_category = Travel. Treat as reopening-sensitive, not a clean fuel-excise primary outcome. |
| `dining_delivery` | hedonic_delivery | semantic_subcat_v2 begins with delivery_. |
| `restaurants_total` | hedonic | clean_category = Restaurants & Dining. |
| `mortgage` | financial_obligations | clean_category = Mortgage. |
| `debit_investment_like` | debit_account_flow_not_true_investment | Raw debit categories Savings, Securities Trades, Investment/Retirement Income, Investment Income, Retirement Contributions, Retirement Income. |

## Cut Start: 12-Week High Top-10 vs Low-Positive Contrast

Largest wallet-share DID-style differences:

| outcome | share_did | high_diff | low_diff |
| --- | --- | --- | --- |
| direct_fuel | -3.62 pp | -3.61 pp | +0.01 pp |
| grocery_ex_fuel | -2.21 pp | -2.57 pp | -0.36 pp |
| travel_total | -1.21 pp | +0.34 pp | +1.56 pp |
| entertainment_ex_gambling | +0.96 pp | +0.26 pp | -0.70 pp |
| mortgage | +0.46 pp | +0.08 pp | -0.38 pp |
| debit_investment_like | -0.40 pp | -1.13 pp | -0.73 pp |
| healthcare_total | -0.40 pp | -0.37 pp | +0.03 pp |
| bnpl_total | -0.39 pp | -0.56 pp | -0.17 pp |

Largest sales-per-active-user DID-style differences:

| outcome | sales_user_did | high_diff | low_diff |
| --- | --- | --- | --- |
| travel_total | $-76.56 | $24.83 | $101.39 |
| restaurants_total | $-27.44 | $92.14 | $119.59 |
| entertainment_ex_gambling | $26.87 | $18.00 | $-8.88 |
| insurance_total | $25.66 | $5.33 | $-20.33 |
| healthcare_total | $-15.53 | $2.55 | $18.08 |
| debit_investment_like | $15.12 | $4.45 | $-10.67 |
| direct_fuel | $-8.27 | $-4.19 | $4.09 |
| grocery_ex_fuel | $-3.61 | $21.39 | $25.00 |

## Restoration: 12-Week High Top-10 vs Low-Positive Contrast

Largest wallet-share DID-style differences:

| outcome | share_did | high_diff | low_diff |
| --- | --- | --- | --- |
| travel_total | +8.49 pp | +7.19 pp | -1.30 pp |
| healthcare_total | +4.26 pp | +4.06 pp | -0.20 pp |
| direct_fuel | -1.73 pp | -1.73 pp | -0.00 pp |
| entertainment_ex_gambling | +1.66 pp | +1.03 pp | -0.63 pp |
| grocery_ex_fuel | -0.97 pp | -0.82 pp | +0.15 pp |
| home_improvement | -0.93 pp | -0.39 pp | +0.54 pp |
| restaurants_total | -0.66 pp | -0.70 pp | -0.03 pp |
| debit_investment_like | -0.39 pp | -0.67 pp | -0.29 pp |

## Investment Side: Monthly Screening Contrast

Monthly grain is coarser than the spending side; event month is treated as post. Use this only for direction finding.

Cut-start 12-week-equivalent window:

| metric | did | high_diff | low_diff |
| --- | --- | --- | --- |
| gross_contribution_per_active_user | $12.68 | $-9.90 | $-22.58 |
| withdrawal_per_active_user | $4.14 | $-16.03 | $-20.17 |
| net_flow_after_withdrawal_fee_per_active_user | $9.61 | $5.35 | $-4.27 |
| signins_per_active_user | -0.047 | +0.089 | +0.136 |
| crypto_portfolio_share | -0.24 pp | -0.54 pp | -0.31 pp |

Restoration 12-week-equivalent window:

| metric | did | high_diff | low_diff |
| --- | --- | --- | --- |
| gross_contribution_per_active_user | $-1.61 | $-12.86 | $-11.24 |
| withdrawal_per_active_user | $20.78 | $20.89 | $0.11 |
| net_flow_after_withdrawal_fee_per_active_user | $-17.81 | $-37.82 | $-20.01 |
| signins_per_active_user | +0.045 | -0.196 | -0.241 |
| crypto_portfolio_share | +0.04 pp | -0.31 pp | -0.35 pp |

## Output Files

- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/exposure_outcomes/exposure_outcome_weekly.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/exposure_outcomes/exposure_outcome_prepost_contrast.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/exposure_outcomes/exposure_outcome_did_contrast.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/exposure_outcomes/investment_exposure_monthly.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/exposure_outcomes/investment_exposure_prepost_contrast.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/exposure_outcomes/investment_exposure_did_contrast.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/exposure_outcomes/outcome_definition_audit.csv`

## Next Method Step

- Convert the strongest rows into user-week event-study regressions with user fixed effects.
- Add pre-period balance plots and placebo event dates.
- Treat travel/reopening-sensitive rows as diagnostics unless the design explicitly models reopening.
