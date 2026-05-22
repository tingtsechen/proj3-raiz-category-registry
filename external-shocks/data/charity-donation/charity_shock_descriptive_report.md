# Charity Donation Shock Descriptive Pack

This report is descriptive only. It uses the aggregate MVP cube to screen whether charity-related subcategories move around crisis, giving-day, and liquidity events.

Two scopes are used:

- `strict`: only `Charitable Giving & Gifts` rows.
- `broad`: all charity-like labels across categories. Broad rows may include op-shop, hospital, RSPCA service, or taxonomy leakage, so use them as diagnostics rather than headline evidence.

## Files

- Event catalog: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/charity_shock_event_catalog.csv`
- Group support: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/charity_group_support.csv`
- Pre/post summary: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/charity_shock_prepost_summary.csv`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_share_of_wallet_4w_event_heatmap.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_participation_rate_4w_event_heatmap.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_black_summer_peak_indexed_timeseries.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_black_summer_peak_4w_diff_bars.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_jobkeeper_announcement_indexed_timeseries.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_jobkeeper_announcement_4w_diff_bars.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_giving_tuesday_now_2020_indexed_timeseries.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_giving_tuesday_now_2020_4w_diff_bars.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_ukraine_appeal_2022_indexed_timeseries.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_ukraine_appeal_2022_4w_diff_bars.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_qld_nsw_floods_telethon_2022_indexed_timeseries.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_qld_nsw_floods_telethon_2022_4w_diff_bars.png`

## Event Catalog

| Event | Date | Family | Notes |
|---|---:|---|---|
| GivingTuesday 2019 | 2019-12-03 | giving_day | Recurring generosity-day shock; overlaps Black Summer bushfire season and December giving. |
| Black Summer bushfire peak attention | 2020-01-05 | disaster | Approximate national-attention anchor during the 2019/20 bushfire response. Use as descriptive only because appeals started earlier and continued for months. |
| JobKeeper announced | 2020-03-30 | liquidity | Liquidity-support announcement. Expected sign is intentionally loose: extra liquidity could raise generosity, but uncertainty could suppress it. |
| Coronavirus Supplement starts | 2020-04-27 | liquidity | JobSeeker Coronavirus Supplement starts. Good candidate for liquidity-without-charity-spillover screening. |
| GivingTuesdayNow COVID response | 2020-05-05 | giving_day | Unscheduled global day of giving and unity in response to COVID-19. |
| GivingTuesday 2021 | 2021-11-30 | giving_day | Recurring generosity-day shock. |
| Ukraine crisis appeal | 2022-02-28 | international_crisis | Australian Red Cross Ukraine appeal launch. Overlaps eastern Australia floods. |
| QLD/NSW floods telethon | 2022-03-12 | disaster | Australia Unites telethon for QLD/NSW floods. Strong overlap with Ukraine appeal. |
| GivingTuesday 2022 | 2022-11-29 | giving_day | Recurring generosity-day shock. |

## Strict Charity Support

| Group | Weeks | Sales | Count | Donor-week sum |
|---|---:|---:|---:|---:|
| Total charity | 266 | $227,067,231 | 3,901,813 | 3,200,346 |
| General/unmatched | 266 | $206,426,360 | 3,326,809 | 2,677,899 |
| World Vision | 266 | $6,340,920 | 111,985 | 103,582 |
| Red Cross | 266 | $3,583,591 | 109,207 | 101,618 |
| St Vincent / religious | 266 | $3,302,062 | 160,291 | 135,763 |
| Oxfam | 265 | $1,766,959 | 43,698 | 41,807 |
| Smith Family | 210 | $1,486,936 | 25,974 | 23,015 |
| Environment | 266 | $1,389,113 | 48,580 | 45,980 |
| UNICEF | 266 | $994,918 | 21,225 | 20,232 |
| Human rights | 233 | $721,700 | 23,340 | 22,574 |
| Salvation Army | 266 | $628,007 | 17,347 | 15,693 |
| Mental health | 257 | $400,249 | 12,721 | 11,594 |

## Largest Target-Group Movements (4-Week, Strict)

| Event | Group | Wallet-share pp diff | Participation pp diff | Count/donor diff | Sales/donor diff |
|---|---|---:|---:|---:|---:|
| Black Summer bushfire peak attention | General/unmatched | -0.064 | -2.621 | -0.009 | 3.13 |
| Black Summer bushfire peak attention | Total charity | -0.063 | -2.643 | -0.016 | 1.58 |
| Coronavirus Supplement starts | Total charity | 0.047 | 1.402 | 0.012 | 1.54 |
| GivingTuesdayNow COVID response | Total charity | 0.047 | 1.548 | 0.013 | -2.63 |
| Coronavirus Supplement starts | General/unmatched | 0.046 | 1.337 | 0.008 | 0.57 |
| GivingTuesdayNow COVID response | General/unmatched | 0.045 | 1.463 | 0.008 | -4.47 |
| GivingTuesday 2019 | Total charity | 0.039 | 1.746 | 0.017 | -2.93 |
| GivingTuesday 2019 | General/unmatched | 0.035 | 1.667 | 0.015 | -4.83 |
| QLD/NSW floods telethon | General/unmatched | -0.026 | -0.423 | 0.021 | -3.94 |
| Ukraine crisis appeal | Total charity | -0.025 | -0.188 | 0.013 | -1.08 |
| GivingTuesday 2022 | General/unmatched | 0.024 | 1.471 | 0.013 | 2.92 |
| QLD/NSW floods telethon | Total charity | -0.023 | -0.416 | 0.016 | -2.72 |
| GivingTuesday 2022 | Total charity | 0.023 | 1.463 | 0.016 | 3.61 |
| JobKeeper announced | General/unmatched | 0.021 | -1.126 | -0.028 | 14.91 |

## Counterintuitive Target Rows (4-Week, Strict)

Expected-up target groups whose wallet share or participation proxy moved down:

| Event | Group | Wallet-share pp diff | Participation pp diff |
|---|---|---:|---:|
| Black Summer bushfire peak attention | Total charity | -0.063 | -2.643 |
| Black Summer bushfire peak attention | General/unmatched | -0.064 | -2.621 |
| JobKeeper announced | Total charity | 0.019 | -1.445 |
| JobKeeper announced | General/unmatched | 0.021 | -1.126 |
| QLD/NSW floods telethon | General/unmatched | -0.026 | -0.423 |
| QLD/NSW floods telethon | Total charity | -0.023 | -0.416 |
| Ukraine crisis appeal | Total charity | -0.025 | -0.188 |
| JobKeeper announced | St Vincent / religious | -0.002 | -0.205 |
| GivingTuesday 2022 | Environment | -0.000 | -0.071 |
| JobKeeper announced | Red Cross | -0.001 | -0.058 |
| Ukraine crisis appeal | Human rights | -0.000 | -0.033 |
| GivingTuesdayNow COVID response | Red Cross | 0.000 | -0.015 |
| JobKeeper announced | Mental health | -0.001 | -0.013 |
| GivingTuesday 2021 | Environment | -0.000 | -0.011 |

## Plots

### charity_strict_share_of_wallet_4w_event_heatmap

![charity_strict_share_of_wallet_4w_event_heatmap](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_share_of_wallet_4w_event_heatmap.png)

### charity_strict_participation_rate_4w_event_heatmap

![charity_strict_participation_rate_4w_event_heatmap](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_participation_rate_4w_event_heatmap.png)

### charity_strict_black_summer_peak_indexed_timeseries

![charity_strict_black_summer_peak_indexed_timeseries](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_black_summer_peak_indexed_timeseries.png)

### charity_strict_black_summer_peak_4w_diff_bars

![charity_strict_black_summer_peak_4w_diff_bars](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_black_summer_peak_4w_diff_bars.png)

### charity_strict_jobkeeper_announcement_indexed_timeseries

![charity_strict_jobkeeper_announcement_indexed_timeseries](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_jobkeeper_announcement_indexed_timeseries.png)

### charity_strict_jobkeeper_announcement_4w_diff_bars

![charity_strict_jobkeeper_announcement_4w_diff_bars](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_jobkeeper_announcement_4w_diff_bars.png)

### charity_strict_giving_tuesday_now_2020_indexed_timeseries

![charity_strict_giving_tuesday_now_2020_indexed_timeseries](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_giving_tuesday_now_2020_indexed_timeseries.png)

### charity_strict_giving_tuesday_now_2020_4w_diff_bars

![charity_strict_giving_tuesday_now_2020_4w_diff_bars](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_giving_tuesday_now_2020_4w_diff_bars.png)

### charity_strict_ukraine_appeal_2022_indexed_timeseries

![charity_strict_ukraine_appeal_2022_indexed_timeseries](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_ukraine_appeal_2022_indexed_timeseries.png)

### charity_strict_ukraine_appeal_2022_4w_diff_bars

![charity_strict_ukraine_appeal_2022_4w_diff_bars](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_ukraine_appeal_2022_4w_diff_bars.png)

### charity_strict_qld_nsw_floods_telethon_2022_indexed_timeseries

![charity_strict_qld_nsw_floods_telethon_2022_indexed_timeseries](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_qld_nsw_floods_telethon_2022_indexed_timeseries.png)

### charity_strict_qld_nsw_floods_telethon_2022_4w_diff_bars

![charity_strict_qld_nsw_floods_telethon_2022_4w_diff_bars](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_charity_donation/plots/charity_strict_qld_nsw_floods_telethon_2022_4w_diff_bars.png)

## Interpretation Guardrails

- This is not causal evidence.
- `strict` is the headline scope; `broad` is useful for taxonomy diagnostics.
- Participation is a proxy because the aggregate cube cannot deduplicate users across multiple charity groups in the same week.
- Ukraine and QLD/NSW floods overlap strongly in late February and March 2022.
- December GivingTuesday events overlap Christmas and, in 2019, Black Summer bushfire attention.

## Next Step

Promote only the most interesting rows into Stage 2 cards. The best Stage 2 candidates are likely:

- QLD/NSW floods: use exposed states or flooded postcodes if geography is available.
- Black Summer bushfires: use smoke/fire/postcode exposure if available and avoid COVID-overlap windows.
- Ukraine appeal: use cause-level placebo rather than geographic control.
- Liquidity shocks: test whether JobKeeper/JobSeeker increased charity, or whether uncertainty suppressed it.