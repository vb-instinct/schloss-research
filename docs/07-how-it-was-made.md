# How it was made, and how it repeats

[Home](../README.md) | Previous: [Limits and caveats](06-limits-and-caveats.md)

## Where the ideas come from

A library of 33 documents about Walter Schloss (182 pages): his talks, memos, interviews, partnership results and articles. We read all of them. Two are the same essay, one is a written summary of a video, and one is a three-page excerpt. The list with notes is in the [source ledger](../sources/corpus-source-ledger.md). Library home: https://www.bishoprockcap.com/library/walter-schloss

## The steps

1. **Discover.** Run free screening tools over the whole market: [TradingView](https://www.tradingview.com) for the US and Australia, [Screener.in](https://www.screener.in) for India. Filters: price at most 0.8 times book value, borrowings at most equal to equity, and positive tangible book.
2. **Recalculate.** For each company we compute tangible book value, price to tangible book (P/TBV) and net current asset value from the screen's own balance-sheet fields.
3. **Remove special cases.** Banks, insurers, property trusts and miners are set aside because their assets need different analysis.
4. **Rank and choose.** The cheapest ratios and the most interesting names go forward for reading.
5. **Read the filings.** Check tangible assets, all debts, leases, cash burn, share count changes, owners and corporate actions in the official reports.
6. **Stress test.** Cut the value of inventory and receivables by 25% to see if the protection holds.
7. **Label.** Each company gets a verdict from [How to read the numbers](04-reading-the-numbers.md).

The technical details of how the screens were built are in [screener rebuild](../screener-setup/screener-rebuild.md).

## The monthly routine (planned)

A refresh is planned for the 1st of each month. Each run should:

- re-run the screens and note which names were added or removed, and why
- check prices, filings, share counts and any corporate actions
- keep last month's snapshot and show what changed
- separate "price moved" from "the assets got weaker"
- publish the coverage counts and say what was not checked
- be a valid result even if no company passes

Full protocol: [monthly protocol](../protocol/monthly-protocol.md).

## The outputs

| Format | Where |
|---|---|
| Plain-English pages | [docs/](01-summary.md) |
| Single-page visual report | [reports/schloss-october-2026.html](../reports/schloss-october-2026.html) |
| Technical notes | [framework](../framework/schloss-framework-and-implementation.md), [markets/](../markets/) |

[Home](../README.md) | Previous: [Limits and caveats](06-limits-and-caveats.md)
