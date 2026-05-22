# Cyber Trust Shock Descriptive Screen

This is a non-COVID screening-lite pack for the 2022 Optus and Medibank cyber breach wave.

Main idea: a privacy / identity-theft shock may trigger defensive switching. For Optus, the direct test is whether `telco_optus` falls and competitor telcos rise. For Medibank, the current taxonomy only supports broad health-insurance rows, not provider-specific Medibank switching.

## Event Anchors

| Event | Date | Interpretation | Source |
|---|---:|---|---|
| Optus data breach public disclosure | 2022-09-22 | Optus publicly disclosed a cyber attack affecting customer data. | https://www.abc.net.au/news/2022-09-22/optus-hit-with-cyber-attack-impacting-customers-/101466036 |
| Optus data-sharing / fraud-monitoring response | 2022-10-06 | Government enabled Optus to share affected ID data with financial institutions; APRA warned regulated entities about identity theft and fraud risk. | https://www.apra.gov.au/optus-data-breach-an-update-for-apra-regulated-entities |
| Medibank cyber incident public disclosure | 2022-10-13 | Medibank publicly disclosed a cyber incident affecting systems and customer data risk. | https://www.abc.net.au/news/2022-10-13/health-insurer-medibank-hit-by-cyber-attack/101531392 |

## Universe Policy

| Universe | Role |
|---|---|
| `telco_affected_optus` | Direct Optus payment row: `Telecom & Internet / telco_optus` |
| `telco_competitors` | Telstra, Vodafone, Dodo, MVNO, and tier-2 ISP rows |
| `health_insurance_primary` | `health_insurance` and `insurance_health`; Medibank diagnostic only, not provider-specific |
| `insurance_context` | General/life/auto/travel insurance context rows |
| `telco_taxonomy_leakage` / `insurance_taxonomy_leakage` | Labels outside their primary categories; audit only |

## Optus Breach: Universe-Level Movement

| Window | Universe | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post | Crosses Medibank? |
|---:|---|---:|---:|---:|---|
| 2 | health_insurance_primary | 0.007 | -1.825 | $6,375,704 -> $5,576,472 | False |
| 2 | insurance_context | 0.103 | 1.273 | $8,540,410 -> $9,131,029 | False |
| 2 | telco_affected_optus | 0.017 | -0.182 | $2,881,211 -> $2,808,003 | False |
| 2 | telco_competitors | 0.035 | -0.608 | $6,828,615 -> $6,578,674 | False |
| 4 | health_insurance_primary | 0.053 | -0.195 | $12,227,057 -> $12,032,379 | True |
| 4 | insurance_context | 0.082 | -0.051 | $17,725,193 -> $17,649,812 | True |
| 4 | telco_affected_optus | 0.023 | -0.063 | $5,611,400 -> $5,545,858 | True |
| 4 | telco_competitors | 0.078 | 0.707 | $13,568,410 -> $14,183,160 | True |
| 8 | health_insurance_primary | 0.035 | -0.120 | $24,538,994 -> $24,282,139 | True |
| 8 | insurance_context | 0.072 | 0.513 | $35,415,158 -> $36,256,392 | True |
| 8 | telco_affected_optus | 0.023 | 0.177 | $11,193,152 -> $11,489,566 | True |
| 8 | telco_competitors | 0.058 | 0.542 | $27,736,777 -> $28,653,935 | True |

## Optus Breach +/-2w: Telco Movers

**Largest decreases**

_No rows._

**Largest increases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| up | Telecom & Internet | `telco_optus` | 0.017 | -0.182 | $2,881,211 -> $2,808,003 |

### Competitors

**Largest decreases**

_No rows._

**Largest increases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| up | Telecom & Internet | `telco_telstra` | 0.019 | -0.433 | $3,845,533 -> $3,664,057 |
| up | Telecom & Internet | `telco_vodafone` | 0.011 | 0.052 | $1,296,569 -> $1,322,711 |
| up | Telecom & Internet | `telco_tier2_isp` | 0.003 | -0.197 | $1,263,674 -> $1,180,471 |
| up | Telecom & Internet | `telco_dodo` | 0.002 | 0.025 | $152,331 -> $163,949 |
| up | Telecom & Internet | `telco_mvno` | 0.000 | -0.054 | $270,508 -> $247,486 |

## Optus Breach +/-4w: Telco Movers

**Largest decreases**

_No rows._

**Largest increases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| up | Telecom & Internet | `telco_optus` | 0.023 | -0.063 | $5,611,400 -> $5,545,858 |

### Competitors

**Largest decreases**

_No rows._

**Largest increases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| up | Telecom & Internet | `telco_telstra` | 0.041 | 0.308 | $7,514,182 -> $7,780,338 |
| up | Telecom & Internet | `telco_vodafone` | 0.017 | 0.254 | $2,495,214 -> $2,720,058 |
| up | Telecom & Internet | `telco_tier2_isp` | 0.013 | 0.107 | $2,475,044 -> $2,568,684 |
| up | Telecom & Internet | `telco_mvno` | 0.004 | 0.021 | $778,938 -> $794,552 |
| up | Telecom & Internet | `telco_dodo` | 0.002 | 0.017 | $305,031 -> $319,528 |

## Optus Response Date +/-2w Diagnostic

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Telecom & Internet | `telco_optus` | -0.012 | -0.179 | $2,808,003 -> $2,737,855 |

**Largest increases**

_No rows._

### Competitors

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Telecom & Internet | `telco_dodo` | -0.001 | -0.020 | $163,949 -> $155,579 |

**Largest increases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| up | Telecom & Internet | `telco_mvno` | 0.017 | 0.663 | $247,486 -> $547,066 |
| up | Telecom & Internet | `telco_telstra` | 0.016 | 0.986 | $3,664,057 -> $4,116,281 |
| up | Telecom & Internet | `telco_tier2_isp` | 0.009 | 0.456 | $1,180,471 -> $1,388,213 |
| up | Telecom & Internet | `telco_vodafone` | 0.000 | 0.154 | $1,322,711 -> $1,397,347 |

## Medibank Incident +/-4w: Health Insurance Diagnostic

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Insurance | `insurance_health` | -0.011 | -0.015 | $12,496,781 -> $12,492,518 |

**Largest increases**

_No rows._

### Insurance Context

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Insurance | `insurance_general` | -0.023 | -0.121 | $17,096,805 -> $17,002,754 |
| down | Insurance | `insurance_life` | -0.006 | -0.228 | $401,712 -> $198,589 |
| down | Automotive & Fuel | `auto_insurance` | -0.001 | -0.031 | $538,209 -> $510,768 |

**Largest increases**

_No rows._

## Taxonomy Leakage Audit

| Category | Universe | Share of universe sales | Subcats |
|---|---|---:|---:|
| Insurance | insurance_taxonomy_leakage | 95.8% | 133 |
| Services | insurance_taxonomy_leakage | 1.5% | 3 |
| Other | insurance_taxonomy_leakage | 1.1% | 3 |
| Loans | insurance_taxonomy_leakage | 0.7% | 1 |
| Restaurants & Dining | insurance_taxonomy_leakage | 0.4% | 3 |
| Personal & Family | insurance_taxonomy_leakage | 0.1% | 3 |
| Entertainment & Recreation | insurance_taxonomy_leakage | 0.1% | 3 |
| Mortgage | insurance_taxonomy_leakage | 0.1% | 3 |
| Rent | insurance_taxonomy_leakage | 0.0% | 3 |
| Utilities | insurance_taxonomy_leakage | 0.0% | 3 |
| Groceries | insurance_taxonomy_leakage | 0.0% | 3 |
| Service Charges & Fees | insurance_taxonomy_leakage | 0.0% | 3 |

## Reading Notes

- Use Optus +/-2w and +/-4w as the main descriptive windows.
- Optus +/-8w crosses Medibank and should be read as combined cyber-panic context.
- Medibank rows are broad health-insurance diagnostics because the current taxonomy does not identify Medibank-specific transactions.
- Lack of Optus decline or competitor rise is itself interesting: switching frictions/contracts may dominate outrage.
- Stage 2 would need user-level pre-breach Optus users vs non-Optus telco users, plus churn/add-on/reallocation outcomes.

## Output Files

- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/cyber_trust_event_catalog.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/cyber_trust_universe_prepost_summary.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/cyber_trust_subcategory_prepost_summary.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/cyber_trust_top_movers.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/cyber_trust_taxonomy_audit.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/cyber_trust_manifest.json`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/plots/cyber_trust_telco_timeseries.png`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/plots/cyber_trust_optus_4w_bars.png`

## Plots

![cyber_trust_telco_timeseries](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/plots/cyber_trust_telco_timeseries.png)

![cyber_trust_optus_4w_bars](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_cyber_trust/plots/cyber_trust_optus_4w_bars.png)
