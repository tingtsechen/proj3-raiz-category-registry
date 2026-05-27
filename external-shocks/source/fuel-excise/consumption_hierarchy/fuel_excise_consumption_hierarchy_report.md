# Fuel Excise Consumption Hierarchy Pack

This is the canonical descriptive pack for Fuel Excise cut and restoration screening.

**Primary headline universe:** domestic clean consumption only. POS-terminal / reopening diagnostics and travel-cycle rows are excluded from headline mover tables.

**POS-terminal warning:** internal `*_foreign_pos` labels are generated from Stage A `pos_terminal` rows matching `^XX\s+\w+`; they are not verified country-code foreign transactions and should not be interpreted as fuel-excise effects.

Reading order:

1. true `cat_clean` big categories;
2. research consumption lenses;
3. clean category x subcategory drilldown.

Headline primary plots and tables exclude labels containing:

`misc, unmatched, transfer, bank, atm, cash_withdrawal, cash_withdraw, pos_terminal`

They also exclude `*_foreign_pos` and Travel reopening-cycle rows; these appear in separate secondary/diagnostic universes.

## Files

- Category summary: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/category_prepost_summary.csv`
- Consumption-lens summary: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/lens_prepost_summary.csv`
- Subcategory summary: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/subcategory_prepost_summary.csv`
- Subcategory top movers: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/subcategory_top_movers.csv`
- Noise audit: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/noise_audit.csv`
- Manifest: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/fuel_excise_consumption_hierarchy_manifest.json`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_category_cut_window_heatmap.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_lens_cut_window_heatmap.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_cut_window_heatmap.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_category_restore_window_heatmap.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_lens_restore_window_heatmap.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_restore_window_heatmap.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_cut_12w_top_movers.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_cut_period_26w_top_movers.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_restore_12w_top_movers.png`
- Plot: `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_restore_recovery_18w_top_movers.png`

## Coverage Checks

- Category layer reports 26 `cat_clean` categories.
- Consumption-lens layer reports 10 research lenses.
- `analysis_universe` separates `primary_domestic`, `secondary_travel_cycle`, and `diagnostic_pos_terminal` rows.
- Minimum plot support: 2 observed weeks per side, 5,000 clean user-weeks, $100,000 clean sales.
- Sparse cube rows are not zero-filled.

## Highest Noise Shares

| Category | Lens | Excluded noise sales share | Excluded noise count share |
|---|---|---:|---:|
| Other | Shopping/home/personal | 100.0% | 100.0% |
| Taxes | Financial obligations | 100.0% | 100.0% |
| Service Charges & Fees | Financial obligations | 100.0% | 100.0% |
| Postage & Shipping | Education/business/pets | 100.0% | 100.0% |
| Mortgage | Utilities/housing/bills | 100.0% | 99.9% |
| Pets | Education/business/pets | 99.6% | 98.6% |
| Subscriptions & Online Services | Hedonic/leisure/dining | 99.5% | 96.4% |
| Automotive & Fuel | Mobility/transport ex-fuel | 99.1% | 99.2% |

## POS-Terminal / Reopening Diagnostic

| Window | Wallet-share pp diff | Pre share | Post share | Pre sales | Post sales |
|---|---:|---:|---:|---:|---:|
| Cut start +/-12w | 8.332 | 1.233% | 9.565% | $86.4M | $804.8M |
| Cut period 26w | 15.425 | 1.811% | 17.236% | $286.7M | $3,946.0M |
| Restoration +/-12w | 0.826 | 24.529% | 25.355% | $2,808.2M | $2,903.4M |
| Restoration recovery 18w | 3.584 | 21.894% | 25.477% | $3,588.5M | $4,193.3M |

## Cut start +/-12w: Primary Domestic Big Categories

| Name | Wallet-share pp diff | Sales/active diff | Count/active diff | Excluded noise sales share |
|---|---:|---:|---:|---:|
| Groceries | -1.113 | -5.432 | -0.1519 | 0.0% |
| Insurance | -0.303 | -0.830 | 0.0002 | 0.0% |
| Electronics & Merchandise | -0.222 | 1.942 | 0.0150 | 0.0% |
| Telecom & Internet | -0.179 | -0.476 | -0.0035 | 0.0% |
| Home Improvement | -0.168 | -1.212 | -0.0179 | 0.0% |
| Services | -0.132 | -2.772 | -0.0267 | 0.0% |
| Restaurants & Dining | -0.127 | -0.246 | -0.0205 | 0.0% |
| Entertainment & Recreation | -0.106 | 0.857 | 0.0458 | 0.0% |
| Loans | -0.064 | 4.166 | 0.0847 | 0.0% |
| Utilities | -0.051 | 0.108 | 0.0010 | 0.0% |

## Cut start +/-12w: Primary Domestic Consumption Lenses

| Name | Wallet-share pp diff | Sales/active diff | Count/active diff | Excluded noise sales share |
|---|---:|---:|---:|---:|
| Essentials: grocery/health | -0.873 | -2.114 | -0.0292 | 0.0% |
| Shopping/home/personal | -0.548 | -1.966 | -0.0288 | 0.0% |
| Utilities/housing/bills | -0.547 | -1.068 | -0.0021 | 0.0% |
| Hedonic/leisure/dining | -0.345 | 0.011 | 0.0150 | 0.0% |
| Direct fuel | -0.191 | 1.186 | -0.0112 | 0.0% |
| Education/business/pets | -0.074 | -1.078 | -0.0179 | 0.0% |
| Financial obligations | -0.064 | 4.166 | 0.0847 | 0.0% |
| Charity/prosocial | -0.005 | -0.048 | -0.0009 | 0.0% |
| Mobility/transport ex-fuel | -0.004 | -0.007 | -0.0001 | 0.0% |

## Cut start +/-12w: Primary Domestic Subcategory Movers

| Direction | Category | Subcategory | Lens | Wallet-share pp diff |
|---|---|---|---|---:|
| down | Groceries | `grocery_supermarket_major` | Essentials: grocery/health | -0.676 |
| down | Insurance | `insurance_general` | Utilities/housing/bills | -0.197 |
| down | Home Improvement | `home_bunnings` | Shopping/home/personal | -0.166 |
| down | Groceries | `grocery_fuel_attached` | Direct fuel | -0.165 |
| down | Loans | `loans_bnpl_afterpay` | Financial obligations | -0.149 |
| down | Groceries | `grocery_supermarket_discount` | Essentials: grocery/health | -0.142 |
| down | Groceries | `grocery_alcohol_attached` | Hedonic/leisure/dining | -0.111 |
| down | Insurance | `insurance_health` | Utilities/housing/bills | -0.105 |
| up | Automotive & Fuel | `auto_fuel_7eleven` | Direct fuel | 0.097 |
| up | Loans | `loans_bnpl_zip` | Financial obligations | 0.093 |

## Cut start +/-12w: Secondary Travel-Cycle Movers

| Direction | Category | Subcategory | Lens | Wallet-share pp diff |
|---|---|---|---|---:|
| up | Travel | `travel_hotel` | Mobility/transport ex-fuel | 0.836 |
| up | Travel | `travel_airline` | Mobility/transport ex-fuel | 0.140 |
| up | Travel | `travel_public_transport` | Mobility/transport ex-fuel | 0.004 |
| down | Travel | `travel_rideshare` | Mobility/transport ex-fuel | -0.000 |
| up | Travel | `travel_apple_misc` | Mobility/transport ex-fuel | 0.000 |

## Cut period 26w: Primary Domestic Big Categories

| Name | Wallet-share pp diff | Sales/active diff | Count/active diff | Excluded noise sales share |
|---|---:|---:|---:|---:|
| Groceries | -1.517 | -7.770 | -0.2180 | 0.0% |
| Electronics & Merchandise | -0.497 | -2.322 | -0.0099 | 0.0% |
| Insurance | -0.302 | 1.276 | 0.0082 | 0.0% |
| Entertainment & Recreation | -0.249 | -1.355 | 0.0092 | 0.0% |
| Home Improvement | -0.242 | -2.016 | -0.0230 | 0.0% |
| Telecom & Internet | -0.200 | 0.743 | 0.0126 | 0.0% |
| Services | -0.185 | -4.439 | -0.0416 | 0.0% |
| Restaurants & Dining | -0.174 | -0.308 | -0.0295 | 0.0% |
| Loans | -0.147 | 4.885 | 0.0829 | 0.0% |
| Utilities | -0.053 | 0.949 | 0.0039 | 0.0% |

## Cut period 26w: Primary Domestic Consumption Lenses

| Name | Wallet-share pp diff | Sales/active diff | Count/active diff | Excluded noise sales share |
|---|---:|---:|---:|---:|
| Essentials: grocery/health | -1.141 | -1.313 | -0.0161 | 0.0% |
| Shopping/home/personal | -0.953 | -8.475 | -0.0657 | 0.0% |
| Hedonic/leisure/dining | -0.630 | -4.080 | -0.0522 | 0.0% |
| Utilities/housing/bills | -0.565 | 3.474 | 0.0251 | 0.0% |
| Direct fuel | -0.213 | 3.494 | -0.0114 | 0.0% |
| Financial obligations | -0.147 | 4.885 | 0.0829 | 0.0% |
| Education/business/pets | -0.043 | 0.277 | -0.0069 | 0.0% |
| Charity/prosocial | -0.005 | -0.025 | -0.0005 | 0.0% |
| Mobility/transport ex-fuel | -0.005 | 0.026 | -0.0001 | 0.0% |

## Cut period 26w: Primary Domestic Subcategory Movers

| Direction | Category | Subcategory | Lens | Wallet-share pp diff |
|---|---|---|---|---:|
| down | Groceries | `grocery_supermarket_major` | Essentials: grocery/health | -0.879 |
| down | Home Improvement | `home_bunnings` | Shopping/home/personal | -0.241 |
| down | Loans | `loans_bnpl_afterpay` | Financial obligations | -0.224 |
| down | Groceries | `grocery_fuel_attached` | Direct fuel | -0.220 |
| down | Groceries | `grocery_alcohol_attached` | Hedonic/leisure/dining | -0.206 |
| down | Groceries | `grocery_supermarket_discount` | Essentials: grocery/health | -0.185 |
| down | Insurance | `insurance_general` | Utilities/housing/bills | -0.181 |
| down | Electronics & Merchandise | `elec_specialty` | Shopping/home/personal | -0.123 |
| down | Insurance | `insurance_health` | Utilities/housing/bills | -0.120 |
| down | Entertainment & Recreation | `ent_gambling_sportsbet` | Hedonic/leisure/dining | -0.113 |

## Cut period 26w: Secondary Travel-Cycle Movers

| Direction | Category | Subcategory | Lens | Wallet-share pp diff |
|---|---|---|---|---:|
| up | Travel | `travel_hotel` | Mobility/transport ex-fuel | 2.007 |
| up | Travel | `travel_airline` | Mobility/transport ex-fuel | 0.171 |
| up | Travel | `travel_transfer_misc` | Mobility/transport ex-fuel | 0.006 |

## Restoration +/-12w: Primary Domestic Big Categories

| Name | Wallet-share pp diff | Sales/active diff | Count/active diff | Excluded noise sales share |
|---|---:|---:|---:|---:|
| Groceries | 0.158 | 6.147 | 0.1252 | 0.0% |
| Electronics & Merchandise | 0.132 | 5.904 | 0.0659 | 0.0% |
| Entertainment & Recreation | 0.077 | 3.134 | 0.0460 | 0.0% |
| Insurance | 0.065 | 2.723 | -0.0013 | 0.0% |
| Home Improvement | 0.056 | 2.290 | 0.0210 | 0.0% |
| Loans | 0.046 | 1.828 | 0.0635 | 0.0% |
| Automotive & Fuel | 0.045 | 1.826 | 0.0352 | 0.0% |
| Education | -0.033 | -1.454 | -0.0013 | 0.0% |
| Telecom & Internet | 0.025 | 0.974 | 0.0079 | 0.0% |
| Utilities | 0.014 | 0.548 | 0.0041 | 0.0% |

## Restoration +/-12w: Primary Domestic Consumption Lenses

| Name | Wallet-share pp diff | Sales/active diff | Count/active diff | Excluded noise sales share |
|---|---:|---:|---:|---:|
| Shopping/home/personal | 0.190 | 8.331 | 0.0914 | 0.0% |
| Essentials: grocery/health | 0.124 | 4.682 | 0.1009 | 0.0% |
| Utilities/housing/bills | 0.101 | 4.070 | 0.0107 | 0.0% |
| Hedonic/leisure/dining | 0.100 | 4.000 | 0.0499 | 0.0% |
| Direct fuel | 0.052 | 2.097 | 0.0432 | 0.0% |
| Financial obligations | 0.046 | 1.828 | 0.0635 | 0.0% |
| Education/business/pets | -0.037 | -1.604 | -0.0175 | 0.0% |
| Mobility/transport ex-fuel | 0.001 | 0.020 | 0.0001 | 0.0% |
| Charity/prosocial | 0.000 | 0.013 | 0.0005 | 0.0% |

## Restoration +/-12w: Primary Domestic Subcategory Movers

| Direction | Category | Subcategory | Lens | Wallet-share pp diff |
|---|---|---|---|---:|
| up | Groceries | `grocery_supermarket_major` | Essentials: grocery/health | 0.093 |
| up | Insurance | `insurance_general` | Utilities/housing/bills | 0.062 |
| up | Home Improvement | `home_bunnings` | Shopping/home/personal | 0.056 |
| up | Loans | `loans_bnpl_afterpay` | Financial obligations | 0.045 |
| up | Entertainment & Recreation | `ent_gambling_sportsbet` | Hedonic/leisure/dining | 0.040 |
| down | Education | `edu_university` | Education/business/pets | -0.033 |
| up | Electronics & Merchandise | `elec_retail_kmart` | Shopping/home/personal | 0.031 |
| up | Groceries | `grocery_alcohol_attached` | Hedonic/leisure/dining | 0.030 |
| up | Electronics & Merchandise | `elec_retail_big_w` | Shopping/home/personal | 0.026 |
| down | Restaurants & Dining | `resto_delivery_deliveroo` | Hedonic/leisure/dining | -0.008 |

## Restoration +/-12w: Secondary Travel-Cycle Movers

| Direction | Category | Subcategory | Lens | Wallet-share pp diff |
|---|---|---|---|---:|
| down | Travel | `travel_hotel` | Mobility/transport ex-fuel | -0.658 |
| up | Travel | `travel_transfer_misc` | Mobility/transport ex-fuel | 0.073 |
| up | Travel | `travel_airline` | Mobility/transport ex-fuel | 0.025 |
| down | Travel | `travel_rideshare` | Mobility/transport ex-fuel | -0.009 |

## Restoration recovery 18w: Primary Domestic Big Categories

| Name | Wallet-share pp diff | Sales/active diff | Count/active diff | Excluded noise sales share |
|---|---:|---:|---:|---:|
| Insurance | -0.182 | -5.152 | -0.0016 | 0.0% |
| Groceries | 0.136 | 10.341 | 0.1451 | 0.0% |
| Electronics & Merchandise | 0.088 | 5.807 | 0.0751 | 0.0% |
| Home Improvement | 0.057 | 2.982 | 0.0304 | 0.0% |
| Loans | 0.038 | 2.884 | 0.0864 | 0.0% |
| Entertainment & Recreation | 0.036 | 2.235 | 0.0278 | 0.0% |
| Restaurants & Dining | -0.029 | -0.557 | -0.0243 | 0.0% |
| Education | -0.025 | -1.039 | -0.0019 | 0.0% |
| Services | -0.007 | -0.187 | -0.0011 | 0.0% |
| Automotive & Fuel | -0.004 | 1.110 | 0.0231 | 0.0% |

## Restoration recovery 18w: Primary Domestic Consumption Lenses

| Name | Wallet-share pp diff | Sales/active diff | Count/active diff | Excluded noise sales share |
|---|---:|---:|---:|---:|
| Utilities/housing/bills | -0.183 | -3.812 | 0.0110 | 0.0% |
| Shopping/home/personal | 0.135 | 8.653 | 0.1092 | 0.0% |
| Essentials: grocery/health | 0.080 | 7.527 | 0.1072 | 0.0% |
| Hedonic/leisure/dining | 0.068 | 4.646 | 0.0382 | 0.0% |
| Financial obligations | 0.038 | 2.884 | 0.0864 | 0.0% |
| Education/business/pets | -0.029 | -1.067 | -0.0124 | 0.0% |
| Direct fuel | -0.010 | 1.118 | 0.0261 | 0.0% |
| Charity/prosocial | -0.001 | -0.014 | 0.0002 | 0.0% |
| Mobility/transport ex-fuel | 0.000 | 0.030 | 0.0001 | 0.0% |

## Restoration recovery 18w: Primary Domestic Subcategory Movers

| Direction | Category | Subcategory | Lens | Wallet-share pp diff |
|---|---|---|---|---:|
| down | Insurance | `insurance_general` | Utilities/housing/bills | -0.175 |
| up | Groceries | `grocery_supermarket_major` | Essentials: grocery/health | 0.063 |
| up | Groceries | `grocery_alcohol_attached` | Hedonic/leisure/dining | 0.061 |
| up | Home Improvement | `home_bunnings` | Shopping/home/personal | 0.058 |
| up | Loans | `loans_bnpl_afterpay` | Financial obligations | 0.042 |
| down | Education | `edu_university` | Education/business/pets | -0.024 |
| up | Electronics & Merchandise | `elec_retail_big_w` | Shopping/home/personal | 0.022 |
| up | Electronics & Merchandise | `elec_retail_kmart` | Shopping/home/personal | 0.021 |
| down | Restaurants & Dining | `resto_delivery_deliveroo` | Hedonic/leisure/dining | -0.013 |
| down | Entertainment & Recreation | `ent_gambling_ladbrokes` | Hedonic/leisure/dining | -0.008 |

## Restoration recovery 18w: Secondary Travel-Cycle Movers

| Direction | Category | Subcategory | Lens | Wallet-share pp diff |
|---|---|---|---|---:|
| down | Travel | `travel_hotel` | Mobility/transport ex-fuel | -0.136 |
| down | Travel | `travel_unmatched` | Mobility/transport ex-fuel | -0.035 |
| up | Travel | `travel_transfer_misc` | Mobility/transport ex-fuel | 0.023 |
| down | Travel | `travel_airline` | Mobility/transport ex-fuel | -0.019 |
| down | Travel | `travel_atm_foreign` | Mobility/transport ex-fuel | -0.013 |
| down | Travel | `travel_rideshare` | Mobility/transport ex-fuel | -0.012 |

## Plots

### fuel_excise_category_cut_window_heatmap

![fuel_excise_category_cut_window_heatmap](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_category_cut_window_heatmap.png)

### fuel_excise_lens_cut_window_heatmap

![fuel_excise_lens_cut_window_heatmap](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_lens_cut_window_heatmap.png)

### fuel_excise_subcategory_cut_window_heatmap

![fuel_excise_subcategory_cut_window_heatmap](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_cut_window_heatmap.png)

### fuel_excise_category_restore_window_heatmap

![fuel_excise_category_restore_window_heatmap](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_category_restore_window_heatmap.png)

### fuel_excise_lens_restore_window_heatmap

![fuel_excise_lens_restore_window_heatmap](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_lens_restore_window_heatmap.png)

### fuel_excise_subcategory_restore_window_heatmap

![fuel_excise_subcategory_restore_window_heatmap](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_restore_window_heatmap.png)

### fuel_excise_subcategory_cut_12w_top_movers

![fuel_excise_subcategory_cut_12w_top_movers](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_cut_12w_top_movers.png)

### fuel_excise_subcategory_cut_period_26w_top_movers

![fuel_excise_subcategory_cut_period_26w_top_movers](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_cut_period_26w_top_movers.png)

### fuel_excise_subcategory_restore_12w_top_movers

![fuel_excise_subcategory_restore_12w_top_movers](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_restore_12w_top_movers.png)

### fuel_excise_subcategory_restore_recovery_18w_top_movers

![fuel_excise_subcategory_restore_recovery_18w_top_movers](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_fuel_excise/consumption_hierarchy/plots/fuel_excise_subcategory_restore_recovery_18w_top_movers.png)

## Guardrails

- This is descriptive screening, not causal evidence.
- Category and lens headline layers now default to `primary_domestic` only.
- POS-terminal / reopening diagnostic rows are not clean fuel-excise outcomes.
- Travel hotel/airline rows are secondary reopening-sensitive outcomes, not primary evidence.
- `n_unique_users` remains a weekly subcategory user count proxy, not a deduplicated person count across weeks.
- Stage 2 still requires a private user-week panel with pre-cut fuel-intensity exposure.