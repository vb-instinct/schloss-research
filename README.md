# Schloss-style value research

**What is this?** A public research project that asks one plain question: *can we find shares that are priced for less than the stuff the company actually owns, and is it safe to rely on that?* It follows the style of Walter Schloss, a famously patient and low-key investor, and applies it to three stock markets: the United States, India (NSE) and Australia (ASX).

**Easiest way to read it:** the rendered site at https://vb-instinct.github.io/schloss-research/

**Snapshot date:** 13 October 2026. This is a one-off first run. Prices and company numbers go stale quickly.

> **Research notes only. This is not investment, tax or legal advice.** Nothing here is a recommendation to buy or sell anything. No trades were made. Read [limits and caveats](docs/06-limits-and-caveats.md) before using anything on this page.

## The short answer

- Screening tools flagged hundreds of "cheap on paper" companies: about 150 in the US, 78 in Australia and 122 in India.
- We then checked a smaller number of them in more depth, to varying degrees. Some checks used the company's own filings; others relied on data websites that were not verified against filings. Which is which is flagged in the technical notes.
- **No company passed every test.** Several looked cheap only because a data vendor's number was wrong, or because the assets behind the price were weaker than they first appeared (store leases, unsold inventory, loans owed to others, shrinking sales).
- A handful are worth a closer look. They are leads for more homework, not conclusions.
- Most flagged companies were **not** examined in depth. This repo says so plainly, name by name.

Full plain-English version: [docs/01 Summary](docs/01-summary.md).

## Read in this order

| # | Page | You will learn |
|---|------|----------------|
| 1 | [Plain-English summary](docs/01-summary.md) | The whole project in about three minutes |
| 2 | [Walter Schloss and his approach](docs/02-schloss-approach.md) | Who he was and what he actually did |
| 3 | [Glossary](docs/03-glossary.md) | Every term, in everyday words |
| 4 | [How to read the numbers](docs/04-reading-the-numbers.md) | What a ratio like "P/TBV 0.56" means, with a worked example |
| 5 | [What we found](docs/05-what-we-found.md) | Company by company, in plain language |
| 6 | [Limits and caveats](docs/06-limits-and-caveats.md) | What was not checked and why you should be careful |
| 7 | [How it was made, and how it repeats](docs/07-how-it-was-made.md) | Method, sources, and the monthly routine |

An illustrated single-page version is here: **[October 2026 report](reports/schloss-october-2026.html)**. (GitHub shows .html files as code. Download it and open it in a browser, or use the rendered version at https://vb-instinct.github.io/schloss-research/reports/schloss-october-2026.html.)

## For analysts: the technical notes

These are the working notes behind the plain-English pages. They are denser, use shorthand, and are kept for checking the work.

- [Screening rules](criteria/criteria.md)
- [Full framework and implementation notes](framework/schloss-framework-and-implementation.md)
- US: [screen](markets/us/us-screen-2026-10-13.md), [diligence](markets/us/diligence-2026-10-13.md)
- India (NSE): [screen](markets/nse/nse-screen-2026-10-13.md), [diligence](markets/nse/diligence-2026-10-13.md)
- Australia (ASX): [summary](markets/asx/asx-summary-2026-10-13.md), [update](markets/asx/asx-update-2026-10-13.md), [diligence](markets/asx/diligence-2026-10-13.md)
- [How the screens were rebuilt](screener-setup/screener-rebuild.md)
- [Reading list of 33 source documents](sources/corpus-source-ledger.md)
- [Monthly protocol](protocol/monthly-protocol.md)

## Frequently asked questions

**Is this telling me what to buy?** No. It shows how a method works and what it turned up. Whether any share suits you depends on your finances, tax, costs and risk tolerance, none of which are covered here.

**Why does "cheap" not mean "good"?** A share can be cheap because the business is shrinking, owes money, or its assets are worth less than the accounts say. Telling the difference is the real work, and it is most of this repo.

**Why do some pages disagree with the screening tool?** Because we rechecked against company filings and found the tool wrong in some cases. Where they differ, the filing wins.

**Is it up to date?** Only as of the snapshot date. Check any price and the latest company report yourself before you rely on a number.

**Does the repo contain private data?** No logins, emails or personal information.
