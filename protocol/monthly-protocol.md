# Monthly research protocol

> **Technical note.** This is the checklist for repeating the research each month. For the plain-English explanation, see [How it was made](../docs/07-how-it-was-made.md).

Updated 14 October 2026. Research only, not personalized financial advice. No trades.

## Timing and scope

Run on the 1st of each month at 9am Australia/Melbourne. Deliver a short summary with a link to the report. Use the latest completed regular exchange session available at research time; do not imply every market has a new close at 9am Melbourne.

Cover ASX, US and NSE ordinary/common equities. State the actual universe accessed, exchange and size gates, returned counts, missing fields and exclusions. A broad vendor scan is not proof of complete exchange coverage. Confirm NSE listing eligibility before calling an Indian discovery result an NSE candidate.

## Repeatable discovery

- NSE: use the saved screen https://www.screener.in/screens/4030427/schloss-nse-base-pb08-de1-mcap250cr/. Query: Market Capitalization > 250 AND Price to book value > 0.01 AND Price to book value < 0.8 AND Debt to equity < 1 AND Book value > 0. Collect all result pages. Prices lack timestamps; P/B is not P/tangible book. Confirm industry and holding-company status on the company page rather than trusting name tags.
- US and ASX: repeat the TradingView scanner specification from the rebuild report. Select stock/common or ADR, 0.0001 <= P/B(fiscal quarter) <= 0.8 and 0 <= D/E(fiscal quarter) <= 1. US gate: NYSE/NASDAQ/AMEX and market cap >= US$30m. ASX gate: ASX and market cap >= A$30m. Record other exclusions rather than treating them as Schloss rules.
- Collect name, description, close, currency, exchange, market cap, P/B, D/E, current assets, all liabilities, equity, goodwill, intangibles, cash/short-term investments, debt, sector and industry. Compute preliminary tangible book and NCAV. Vendor data anomalies, including very low P/B or inconsistent computed ratios, go into an anomaly list for review, not a silent deletion.
- Separate financials, holding companies, mining and other specialist assets. They are not blanket Schloss exclusions; they need different asset analysis.

## Mandatory filing diligence

A scanner hit is a candidate, not a verified pass. Read primary filings for shortlisted names and recheck carried-forward names.

1. Tangible common equity: equity attributable to ordinary shareholders minus goodwill, intangibles and applicable preferred interests. Reconcile common classes, minority interests and corporate actions. Show audited book separately from a conservative asset stress test.
2. NCAV: current assets minus ALL liabilities and senior claims not already deducted. Never subtract borrowings alone. Net-net threshold: market cap <= two-thirds NCAV.
3. Asset tiers: P/tangible common book <=0.80 baseline and <=0.67 strict. These are our reproducible adaptations, not universal rules published by Schloss.
4. Reconcile issued and diluted shares, rights issues, options, ADR ratios and subsequent distributions. Do not mix old equity with new share counts or ignore ex-dividend asset reductions.
5. Check leases, deferred-tax assets, inventories, receivables, restricted cash, investments, contingent claims, pensions, rehabilitation costs, covenants and ongoing cash burn. Investment securities are not cash.
6. Review business and operating history, why the stock is cheap, governance, related-party dealings and whether assets can benefit minority shareholders. Insider ownership alone does not establish protection.
7. Verify price source, date, time, currency and regular-session status. Undated vendor quotes remain undated and cannot certify a current pass. Verify long price history where available; a 52-week low is not a multi-year low.
8. Check subsequent announcements, results releases and changes since the balance sheet. Mark unresolved evidence explicitly.

## Report contents

Lead with the research conclusion, including a no-buy month when warranted. Include:

- Research date, price/fundamental dates and a research-only notice.
- Coverage and missing-data counts by market, discovery gates and specialist exclusions.
- Per-market ranked research candidates with stable identifiers, units, calculations, primary source links, risks and verdicts: numerical pass, conditional, watch, excluded or unverified.
- Changes since last month: additions, removals and reasons. Separate price changes from asset erosion, dilution and distributions.
- A framework/method section that distinguishes original Schloss principles from our numeric implementation.
- Corpus coverage and scope quirks when referring to the original 33-PDF library. Do not claim review of publications or video recordings beyond the supplied material.
- An evidence ledger and unresolved checks. Preserve previous snapshots.

## Required HTML delivery

## Output format

The monthly report is published as a readable page (plain-English summary first, technical detail after) and as a portable HTML file kept in `reports/`, with the monthly snapshot retained. Both use the same verified data. Check the layout on a phone-width screen and a desktop screen, and check that links work.

Keep credentials, account emails, sign-in links and personal information out of public files. Before calling a monthly run complete, confirm the update has actually landed in the repository.

## Monthly results table and checked-data revisions

Maintain `monthly-results.html` as the public plain-language results page. Every scheduled run appends the month for US, NSE and ASX and republishes both this table and the HTML report. Keep it linked from the README and reader navigation.

For each market record discovery counts, actual coverage and missing data. For selected named results record month, market, ticker/name, baseline/strict/net-net numerical status, research verdict, change versus last month, price date, statement date and source link. Separate vendor hits from filing-checked names. NSE P/B hits are not tangible-book hits. Label indicative or stale prices, unverified tests and specialist cases. Do not invent a complete named list from summary counts. The first month has no prior comparison.

When newly published filings, prices, corporate actions or corrected vendor fields are checked during a run or a separately assigned update, revise affected rows promptly after verification. Record revision date, evidence and reason, distinguishing price change from book erosion, dilution or distributions. Retain the prior report snapshot and repository history. New externally published data alone does not mean the table has refreshed. No continuous/live feed is claimed. If event-driven monitoring is requested, establish its sources, cadence and coverage separately.

Use the same verified data for the hosted File, repository HTML report and table. Verify all table content at 320px, 390px and 1280px, using stacked labeled rows on phones. After committing, verify raw files and the rebuilt live page, source links and navigation before reporting completion. Research-only verdicts remain valid even when no buy is certified.
