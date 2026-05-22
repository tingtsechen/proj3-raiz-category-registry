# Treasury Crypto Regulation Consultation Descriptive Screen

This is a non-COVID screening-lite pack for the 2022 Australian crypto-regulation consultation.

Event: Treasury opened consultation on **Crypto asset secondary service providers: Licensing and custody requirements** on 2022-03-21. The consultation ran to 2022-05-27.

Main candidate idea: regulatory scrutiny may reduce crypto exchange funding or shift users across exchange brands. The short windows are the cleanest; 8w/12w post windows cross the 2022-05-09 LUNA collapse and should be treated as confounded.

Source: https://treasury.gov.au/consultation/c2022-259046

## Universe Policy

| Universe | Role |
|---|---|
| `all_crypto_like` | Aggregate of primary crypto services plus crypto exchange labels found anywhere in the taxonomy |
| `primary_crypto_services` | Cleanest row: `Services / services_crypto` |
| `crypto_exchange_taxonomy_leakage` | Exchange-brand labels outside Services, e.g. Binance, CoinSpot, Coinbase, Swyftx; useful but category placement is not interpretable |

## Consultation Opening: Universe-Level Movement

| Window | Universe | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post | Crosses LUNA? |
|---:|---|---:|---:|---:|---|
| 2 | all_crypto_like | -0.014 | -0.304 | $930,539 -> $799,837 | False |
| 2 | crypto_exchange_taxonomy_leakage | -0.005 | -0.094 | $687,224 -> $651,292 | False |
| 2 | primary_crypto_services | -0.008 | -0.211 | $243,315 -> $148,545 | False |
| 4 | all_crypto_like | -0.014 | -0.456 | $2,012,843 -> $1,587,879 | False |
| 4 | crypto_exchange_taxonomy_leakage | -0.001 | -0.071 | $1,415,984 -> $1,346,812 | False |
| 4 | primary_crypto_services | -0.014 | -0.385 | $596,859 -> $241,067 | False |
| 8 | all_crypto_like | -0.029 | -0.502 | $4,517,622 -> $3,523,941 | True |
| 8 | crypto_exchange_taxonomy_leakage | -0.006 | 0.040 | $3,023,315 -> $3,034,270 | True |
| 8 | primary_crypto_services | -0.023 | -0.541 | $1,494,308 -> $489,671 | True |
| 12 | all_crypto_like | -0.054 | -0.839 | $7,444,016 -> $5,017,555 | True |
| 12 | crypto_exchange_taxonomy_leakage | -0.020 | -0.122 | $4,739,260 -> $4,302,041 | True |
| 12 | primary_crypto_services | -0.035 | -0.717 | $2,704,756 -> $715,514 | True |

## Consultation Opening +/-4w: Crypto-Like Movers

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Services | `services_crypto` | -0.014 | -0.385 | $596,859 -> $241,067 |

**Largest increases**

_No rows._

### Exchange-Brand Taxonomy Leakage

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Other | `other_misc_crypto_swyftx` | -0.003 | -0.087 | $185,956 -> $105,331 |
| down | Education | `education_misc_crypto_binance` | -0.003 | -0.073 | $204,870 -> $138,098 |
| down | Travel | `travel_misc_crypto_binance` | -0.000 | -0.018 | $165,717 -> $148,561 |
| down | Other | `other_misc_crypto_coinspot` | -0.000 | -0.005 | $71,709 -> $66,693 |

**Largest increases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| up | Other | `other_misc_crypto_binance` | 0.005 | 0.105 | $513,322 -> $606,950 |

## Consultation Opening +/-8w: Crypto-Like Movers

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Services | `services_crypto` | -0.023 | -0.541 | $1,494,308 -> $489,671 |

**Largest increases**

_No rows._

### Exchange-Brand Taxonomy Leakage

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Education | `education_misc_crypto_binance` | -0.005 | -0.113 | $451,551 -> $240,978 |
| down | Other | `other_misc_crypto_swyftx` | -0.003 | -0.052 | $395,567 -> $294,018 |
| down | Restaurants & Dining | `restaurants_dining_misc_crypto_coinjar` | -0.001 | -0.025 | $75,485 -> $28,214 |
| down | Travel | `travel_misc_crypto_binance` | -0.001 | -0.007 | $313,973 -> $297,167 |
| down | Telecom & Internet | `telecom_internet_misc_crypto_swyftx` | -0.000 | -0.000 | $27,449 -> $26,222 |

**Largest increases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| up | Other | `other_misc_crypto_binance` | 0.005 | 0.216 | $1,034,755 -> $1,400,911 |
| up | Service Charges & Fees | `service_charges_fees_misc_crypto_binance` | 0.001 | 0.037 | $95,147 -> $159,053 |
| up | Other | `other_misc_crypto_coinspot` | 0.000 | 0.025 | $180,482 -> $220,433 |
| up | Loans | `loans_misc_crypto_coinspot` | 0.000 | 0.012 | $91,675 -> $111,058 |

## Consultation Close +/-4w Diagnostic

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Services | `services_crypto` | -0.003 | -0.064 | $265,282 -> $211,113 |

**Largest increases**

_No rows._

### Exchange-Brand Taxonomy Leakage

**Largest decreases**

| Direction | Category | Subcategory | Wallet-share pp diff | Sales/active-user diff | Sales pre -> post |
|---|---|---|---:|---:|---:|
| down | Other | `other_misc_crypto_binance` | -0.006 | -0.114 | $931,487 -> $835,434 |
| down | Other | `other_misc_crypto_coinspot` | -0.005 | -0.145 | $184,214 -> $56,870 |
| down | Travel | `travel_misc_crypto_binance` | -0.004 | -0.109 | $138,358 -> $42,418 |
| down | Other | `other_misc_crypto_swyftx` | -0.003 | -0.094 | $173,003 -> $90,975 |
| down | Service Charges & Fees | `service_charges_fees_misc_crypto_binance` | -0.003 | -0.091 | $119,342 -> $39,233 |
| down | Education | `education_misc_crypto_binance` | -0.002 | -0.046 | $103,256 -> $63,334 |

**Largest increases**

_No rows._

## Taxonomy Audit

| Category | Universe | Crypto sales share | Crypto count share | Subcats |
|---|---|---:|---:|---:|
| Services | primary_crypto_services | 44.6% | 55.4% | 1 |
| Other | crypto_exchange_taxonomy_leakage | 21.5% | 16.9% | 6 |
| Loans | crypto_exchange_taxonomy_leakage | 13.5% | 9.0% | 6 |
| Travel | crypto_exchange_taxonomy_leakage | 4.4% | 3.0% | 6 |
| Restaurants & Dining | crypto_exchange_taxonomy_leakage | 3.9% | 4.0% | 6 |
| Service Charges & Fees | crypto_exchange_taxonomy_leakage | 3.8% | 3.2% | 6 |
| Education | crypto_exchange_taxonomy_leakage | 3.2% | 3.1% | 5 |
| Entertainment & Recreation | crypto_exchange_taxonomy_leakage | 2.1% | 1.5% | 6 |
| Telecom & Internet | crypto_exchange_taxonomy_leakage | 0.6% | 0.9% | 5 |
| Personal & Family | crypto_exchange_taxonomy_leakage | 0.6% | 0.7% | 5 |
| Subscriptions & Online Services | crypto_exchange_taxonomy_leakage | 0.3% | 0.5% | 6 |
| Electronics & Merchandise | crypto_exchange_taxonomy_leakage | 0.3% | 0.6% | 5 |

## Reading Notes

- Treat +/-2w and +/-4w around 2022-03-21 as the main descriptive windows.
- Treat +/-8w and +/-12w as contaminated by LUNA, broader crypto drawdown, and RBA first hike.
- `crypto_exchange_taxonomy_leakage` is behaviorally useful but category placement is not meaningful; do not interpret `Other`, `Loans`, or `Travel` literally.
- A Stage 2 version should use user-level pre-consultation crypto exposure and compare exposed vs unexposed users, ideally on both spending-side exchange funding and investment-side Crypto fund behavior.

## Output Files

- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/crypto_reg_event_catalog.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/crypto_reg_universe_prepost_summary.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/crypto_reg_subcategory_prepost_summary.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/crypto_reg_top_movers.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/crypto_reg_taxonomy_audit.csv`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/crypto_regulation_manifest.json`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/plots/crypto_reg_wallet_share_timeseries.png`
- `/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/plots/crypto_reg_consultation_4w_bars.png`

## Plots

![crypto_reg_wallet_share_timeseries](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/plots/crypto_reg_wallet_share_timeseries.png)

![crypto_reg_consultation_4w_bars](/Users/tingtsechen/second-brain/outputs/proj3-raiz-exploration/shock_screening/stage2_crypto_regulation/plots/crypto_reg_consultation_4w_bars.png)
