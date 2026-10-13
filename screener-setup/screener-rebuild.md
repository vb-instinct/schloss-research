# Schloss screen rebuild on free full-universe screeners

Run date: Tuesday 13 October 2026, ~9:20pm AEDT. Research only - not personal financial advice. All figures are screener/vendor data, fiscal-quarter fundamentals, undated quotes; verify against primary filings before any decision.

## Accounts created (agent-operated, free tier)

| Tool | Login | Email verified | Vault entry | Free plan |
|---|---|---|---|---|
| TradingView | (agent account email, redacted) | Yes (clicked activation link, redirected via account_activate) | (vault entry, redacted) (login, agent-designated) | Basic $0 |
| Screener.in | (agent account email, redacted) | Yes (activation link clicked, landed on dashboard) | (vault entry, redacted) (login, agent-designated) | Hobby Investor Rs.0 |

Credentials generated at random and stored only in the vault; never in chat. Both logins were saved into the cloud-browser profile (config-h) on lease release, so future runs start signed in.

## What worked

- **TradingView screener (US + ASX)** - full-universe, no paywall hit. Used the scanner endpoint the screener page itself uses (scanner.tradingview.com/{america,australia}/scan) from the signed-in page: filter on type=common/ADR stock, 0 < P/B(fq) <= 0.8, 0 <= D/E(fq) <= 1, then computed tangible book (equity - goodwill - intangibles), P/TBV, NCAV and net-net (mcap <= 2/3 x (current assets - all liabilities)) per name. Saved-login profile means the monthly run can repeat this verbatim.
- **Screener.in (NSE)** - custom query screen over the full Indian universe. Query: `Market Capitalization > 250 AND Price to book value > 0.01 AND Price to book value < 0.8 AND Debt to equity < 1 AND Book value > 0`. Saved as a reusable screen: https://www.screener.in/screens/4030427/schloss-nse-base-pb08-de1-mcap250cr/ (private to the account).

## Coverage counts

| Market | Tool | Base pass (P/B<=0.8, D/E<=1) | Size/exchange gate | Qualified (tangible book > 0, data sane) | Strict P/TBV<=0.67 | Net-net |
|---|---|---|---|---|---|---|
| US | TradingView | 1089 (all listed common, incl. OTC) | NYSE/NASDAQ/AMEX, mcap >= $30m -> 270 | 238 | 150 | 23 |
| ASX | TradingView | 312 | ASX only, mcap >= A$30m -> 133 | 119 | 78 | 2 |
| NSE | Screener.in | 158 (mcap > Rs.250 cr built in) | - | 158 | 122 (by P/B; TBV split n/a) | n/a (see limits) |

Sector mix worth knowing: US qualified list holds 58 finance names and 11 miners; ASX holds 34 finance and 40 miners/energy. These get separate asset analysis per the framework, not plain P/TBV verdicts.

## US shortlist (ex-finance, ex-miners, by P/TBV)

| Symbol | Name | Last | Mcap $m | P/TBV | D/E | |
|---|---|---|---|---|---|---|
| NASDAQ:HOLO | MicroCloud Hologram Inc. | 1.42 USD | 32.5 | 0.09 | 0.02  | NET-NET |
| NASDAQ:AIFC | AI Financial Corporation | 0.4233 USD | 59.2 | 0.09 | 0.04 |  |
| NASDAQ:MLGO | MicroAlgo, Inc. | 2.88 USD | 35.8 | 0.12 | 0.02  | NET-NET |
| NASDAQ:PSEC | Prospect Capital Corporation | 1.73 USD | 923.5 | 0.20 | 0.41 |  |
| NASDAQ:WATR | Air Water Ventures Limited | 1.9 USD | 60.1 | 0.24 | 0.00 |  |
| NYSE:DLNG | Dynagas LNG Partners LP | 3.57 USD | 129.9 | 0.26 | 0.51 |  |
| NASDAQ:BOOM | DMC Global Inc. | 5.6 USD | 115 | 0.27 | 0.44 |  |
| NASDAQ:CAAS | China Automotive Systems, Inc. | 4.63 USD | 139.7 | 0.28 | 0.17  | NET-NET |
| NYSE:CATO | Cato Corporation (The) | 2.39 USD | 47.6 | 0.28 | 0.83 |  |
| NASDAQ:GDHG | Golden Heaven Group Holdings Ltd. | 1.12 USD | 66.6 | 0.31 | 0.01  | NET-NET |
| NASDAQ:LNZA | LanzaTech Global, Inc. | 6.1 USD | 79.8 | 0.31 | 0.11 |  |
| NASDAQ:SFWL | Shengfeng Development Limited | 8.45 USD | 46.5 | 0.31 | 0.70 |  |
| NYSE:CLVT | Clarivate Plc | 1.61 USD | 1029.9 | 0.32 | 0.94 |  |
| NASDAQ:MYPS | PLAYSTUDIOS, Inc. | 4.23 USD | 50.8 | 0.33 | 0.03 |  |
| NASDAQ:SLMT | Brera Holdings PLC | 3.17 USD | 34.9 | 0.33 | 0.00 |  |

Notes: HOLO/MLGO/AIFC are tiny Chinese ADRs - expect data-quality and governance risk; CATO (0.28) matches the prior run's lease-impaired deep-discount case; HURC cross-check: this pipeline computes P/TBV 0.72 vs prior manual 0.756 - consistent. US net-nets (23) include CAAS, DSWL, LGIH (mcap $1.0b, D/E 0.74), PHUN, INVE.

## ASX shortlist (ex-finance, ex-miners, by P/TBV)

| Symbol | Name | Last | Mcap A$m | P/TBV | D/E | |
|---|---|---|---|---|---|---|
| ASX:OMH | OM Holdings Ltd. | 0.2 AUD | 152.9 | 0.23 | 0.41 |  |
| ASX:MCA | Murray Cod Australia Limited | 0.14 AUD | 34.7 | 0.28 | 0.29 |  |
| ASX:DBF | Duxton Farms Limited | 0.34 AUD | 37 | 0.33 | 0.96 |  |
| ASX:A1N | ARN Media Limited | 0.28 AUD | 90.5 | 0.37 | 0.62 |  |
| ASX:DGL | DGL Group Limited | 0.255 AUD | 72.7 | 0.39 | 0.62 |  |
| ASX:OCA | Oceania Healthcare Ltd. | 0.535 AUD | 383.8 | 0.39 | 0.45 |  |
| ASX:LLC | Lendlease Group | 2.42 AUD | 1699.8 | 0.40 | 0.97 |  |
| ASX:SM1 | Synlait Milk Ltd. | 0.36 AUD | 218 | 0.40 | 0.39 |  |
| ASX:SHJ | Shine Justice Ltd. | 0.63 AUD | 112.6 | 0.43 | 0.38 |  |
| ASX:ZGL | Zicom Group Limited | 0.15 AUD | 32.3 | 0.44 | 0.24 |  |
| ASX:RYM | Ryman Healthcare Ltd. | 1.44 AUD | 1491.1 | 0.44 | 0.39 |  |
| ASX:NVX | NOVONIX Ltd | 0.087 AUD | 89.8 | 0.44 | 0.63 |  |
| ASX:AAC | Australian Agricultural Company Li | 1.31 AUD | 786.3 | 0.44 | 0.29 |  |
| ASX:VMT | Vmoto Limited | 0.07 AUD | 30.2 | 0.45 | 0.37 |  |
| ASX:SNZ | Summerset Group Holdings Limited | 5.6 AUD | 1335.4 | 0.46 | 0.59 |  |

Prior-run cross-checks: IRI P/TBV 0.51 at A$0.275 (matches the ASX-feed price the earlier worker verified), CAA P/TBV 0.78 (borderline, ex-DTA it failed before), GRR net-net on the numbers (mcap A$127m vs NCAV A$332m) but stays a specialist mining watch, not a plain net-net buy.

## NSE shortlist (Screener.in, operating companies, by P/B)

| Name | P/B | D/E | Mcap Rs.cr |
|---|---|---|---|
| Rajesh Exports | 0.09 | 0.06 | 1588 |
| Reliance Infra. | 0.13 | 0.28 | 2326 |
| Veritas (India) | 0.13 | 0.15 | 368 |
| Brightcom Group | 0.17 | 0.00 | 1826 |
| Hexa Tradex | 0.19 | 0.00 | 856 |
| Oswal Green Tech | 0.20 | 0.00 | 489 |
| Hinduja Global | 0.20 | 0.24 | 1679 |
| Orient Paper | 0.22 | 0.20 | 340 |
| GFL | 0.23 | 0.00 | 634 |
| Zuari Industries | 0.23 | 0.75 | 820 |
| Coffee Day Enter | 0.24 | 0.30 | 664 |
| Uniphos Enter. | 0.25 | 0.00 | 598 |
| Mishtann Foods | 0.25 | 0.05 | 332 |
| Rajapalayam Mill | 0.29 | 0.47 | 679 |
| Dhunseri Vent. | 0.30 | 0.29 | 977 |
| Kothari Products | 0.31 | 0.09 | 369 |
| Vardhman Hold. | 0.31 | 0.00 | 1161 |
| Den Networks | 0.32 | 0.01 | 1289 |
| Jain Irrigation | 0.32 | 0.74 | 1922 |
| Riddhi Siddhi Gl | 0.33 | 0.19 | 516 |

All three prior NSE candidates reproduce: DEN Networks P/B 0.32, GSFC 0.48 (prior audited-book estimate 0.482), Maithan Alloys 0.63 (prior 0.626). 21 of 158 hits are investment/holding/finance names by name-tagging (Nalwa Sons, Kalyani Invest, BF Investment, Elcid, JSW Holdings, Pilani, VLS Finance, General Insurance, PTC India Fin etc.) - separate analysis per the framework. The name-based tag misses some holdcos (e.g. Hexa Tradex, Uniphos, Dhunseri Ventures, Vardhman Holdings look like holdcos but pass the regex) - free tier has no industry column in results, so confirm sector on the company page during diligence.

## What the free tiers could not do

- **Screener.in free**: no CSV export (premium, Rs.4,999/yr - confirmed by hitting the premium gate on Download Results); no industry column in screen results; custom-ratio formula builder rejects balance-sheet liability terms ('Total liabilities', 'Borrowings', 'Other liabilities' all rejected - only 'Current assets' and 'Debt' accepted), so a true NCAV/net-net ratio cannot be built; P/B is book (not tangible book) - goodwill/intangibles stripping happens in diligence; no quote timestamps.
- **TradingView free**: scanner fundamentals are fiscal-quarter vendor data without date stamps; India coverage is materially incomplete (P/B, D/E, balance-sheet fields are null for GSFC, Maithan, DEN and most NSE names - that is why NSE runs on Screener.in instead); no native tangible-book ratio (computed from equity - goodwill - intangibles client-side); saved-screen and layout limits on Basic plan not yet probed; ads.
- **Both**: no 10-20-year operating-history filter, no 'why is it cheap' data, no lease/deferred-tax/cash-burn adjustments. Those stay in the per-name diligence step, unchanged from the current framework.

## Monthly run handoff

1. NSE: sign into Screener.in (vault login), open the saved screen URL above, sort by 'Price to book value', collect all pages (158 names this run), tag financials/holdcos, verify strict-tier names against audited filings.
2. US/ASX: sign into TradingView (vault login), POST to scanner.tradingview.com/{america,australia}/scan from the signed-in screener page with columns [name, description, close, currency, exchange, market_cap_basic, price_book_fq, debt_to_equity_fq, total_current_assets_fq, total_liabilities_fq, total_equity_fq, goodwill_fq, intangible_assets_fq, cash_n_short_term_invest_fq, total_debt_fq, sector, industry], filters type=stock, subtype in (common, adr), 0.0001 <= price_book_fq <= 0.8, 0 <= debt_to_equity_fq <= 1; gate to major exchanges + mcap floor ($30m / A$30m); compute TBV, P/TBV, NCAV, net-net; drop vendor-P/B < 0.03 or computed P/TBV > 1.2 as bad data.
3. Verdicts stay research-only: pass / conditional / watch / excluded / unverified, with a no-buy month a valid result.

Data provenance: TradingView scanner API (in-page, signed-in session, 13 Oct 2026 ~9:15-9:20pm AEDT) and Screener.in screen results (same session). No primary filings were re-read in this run; this rebuild replaces the discovery step, not the diligence step.
