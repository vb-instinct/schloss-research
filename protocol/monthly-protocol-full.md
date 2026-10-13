# Schloss monthly research protocol

Updated 13 October 2026. Research only, not personalized financial advice. No trades.

## Timing and scope

Run on the 1st of each month at 9am Australia/Melbourne. Deliver a short WhatsApp summary with the hosted report link. Use the latest completed regular exchange session available at research time; do not imply every market has a new close at 9am Melbourne.

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

The final output is polished, mobile-friendly HTML, not Markdown-only.

Produce both:

1. A hosted File with a usable canonical link.
2. A portable HTML report for the public research repository vb-instinct/schloss-research, retaining the monthly snapshot. Keep assets bundled or provided beside the HTML with valid relative paths. Do not depend on an authenticated report viewer for the portable version.

Use the same verified report data for both versions. Fit core facts and caveats within a phone's width using cards or labeled rows; reserve wide tables for supplemental datasets. Use clear headings, readable type, source links, freshness labels and restrained styling. Inspect all sections at 320px, 390px and 1280px; check navigation, disclosures and source links. Fix clipping, overflow, missing assets and inaccessible content before delivery.

Keep credentials, account emails, vault details, sign-in links, private conversation material and unrelated personal information out of public artifacts. Preserve the hosted File's existing audience unless a separate instruction changes it. Making the repository public does not automatically change the hosted File's access.

Return the hosted link, portable HTML attachment and the short WhatsApp summary. Repository publication and recurring delivery must be checked to have landed before calling the monthly run complete.
