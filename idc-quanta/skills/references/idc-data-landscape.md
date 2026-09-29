# IDC Data Landscape

Read this file before the first structured-data query on any market you have not queried yet this session, and whenever a user asks "what data do you have", "what markets does IDC cover", or "Tracker or Spending Guide?". It explains how IDC's supply-side and demand-side data is organized and how to choose the right library from the live catalogue.

This file deliberately names no libraries. IDC adds and renames data products over time, so the connector's live catalogue is the only authoritative list of what exists, what it is called, and which ID it carries. Request it once per session and choose from it.

## How IDC data is organized

IDC produces two kinds of content, and this connector reaches both.

- **Structured data** - queryable numbers: market size, vendor revenue and share, growth, CAGR, shipments, spend. Organized as Library -> Dataset -> Profile -> Query. Resolve a profile before you query.
- **Qualitative research** - narrative documents: MarketScapes, Market Perspectives, Forecasts, FutureScapes, surveys. Retrieved and read for context, positioning, and analyst judgment.

Most strong answers use both: structured data for the cited number, research for the "why".

## Choosing the data source: Tracker vs Spending Guide

This is the most common source-selection error, so decide deliberately.

- **Tracker = supply side (what vendors sell).** Use for a technology product market: market size, vendor revenue, vendor share, unit shipments, growth of a product market. "How big is the cloud IaaS market?", "who leads in security products?", "what is the CAGR for AI software?"
- **IT Spending Guide = demand side (what buyers spend).** Use for IT budgets and spend allocation by industry, vertical, or category. "How much is the banking industry spending on AI?" is a Spending Guide question, not a Tracker question. "What share of retail IT spend goes to cloud?", "what is the DX spend CAGR for healthcare?"

Quick test: if the subject is a vendor or a product market, reach for a Tracker. If the subject is an industry's or buyer segment's budget, reach for a Spending Guide. Many questions want both - size the market with a Tracker, then show who is buying with a Spending Guide.

All Spending Guide data is at industry, segment, or category level. None of it is named-account or company-specific.

For a broad, multi-segment IT spending outlook, look in the catalogue for IDC's cross-market IT spending forecast rather than stitching together individual Trackers.

## Choosing a library from the live catalogue

1. **Decide the side first** (Tracker or Spending Guide), using the section above.
2. **Shortlist by name and scope.** From the catalogue listing, keep only the libraries whose names match the market, technology, industry or category in the question. Do not work through the whole catalogue.
3. **Where two libraries overlap, take the most specific one that actually breaks out what was asked.** A dedicated tracker for the exact market beats a broad tracker that contains it (a cloud IaaS tracker over a general public cloud services tracker for an IaaS question). Judge specificity by the library's dimensions, not its name alone: if the first pick has no value for the asked segment, check the runner-up before concluding. For Spending Guides, prefer the guide whose dimensions carry both the industry and the technology asked. A vertical guide beats a cross-industry one only when it breaks out that technology; otherwise take the technology guide and filter it to the industry, which may sit one level down in its industry hierarchy.
4. **Where two are equally specific, take the more recently published one** and confirm the period from the query response itself.
5. **Confirm entitlement** before promising data from a library (Rule 12).
6. **If the choice is still genuinely unclear**, query the stronger candidate, and say in one line which data product the figure comes from so the reader can judge the scope.

## Question-to-source matrix

| Question shape | Source | Notes |
|---|---|---|
| "How big is the X market?" | Tracker (SUM) | Filter by year and geography |
| "CAGR / forecast for X?" | Tracker (CAGR) | Use a Forecast dataset to the horizon year |
| "Who leads / share in X?" | Tracker (SHARE) | Vendor revenue share within the market total |
| "How does [vendor] compare to the market?" | Tracker | Vendor revenue plus total market in one query |
| "How much is [industry] spending on [tech]?" | Spending Guide | Pick the vertical or category guide |
| "IT budget CAGR for [vertical]?" | Spending Guide (CAGR) | Vertical-specific guide where one exists |
| "What share of IT spend goes to [category]?" | Spending Guide (SHARE) | Allocation of buyer spend, not vendor share |
| "IDC's view / take on X trend or vendor?" | Search documents | Narrative, not structured figures |
| "Is there a MarketScape / report on X?" | Search documents | Filter by content group |
| "What libraries/trackers cover X?" | The connector's catalogue listing | Answer from the live listing, never from memory |

## No-Tracker fallback

If neither a Tracker nor a Spending Guide covers the market (for example an emerging category like quantum computing):

1. Confirm from the catalogue listing that nothing matches.
2. Pivot to document search for narrative market sizing from IDC research.
3. Extract the figure from the document, cite the document and date, and present at **Medium** confidence.
4. Record the gap in the answer: "No IDC Tracker or Spending Guide covers this market; the figure is from IDC research."

Never fill a no-Tracker gap with training-data numbers.

## Coverage limits

When a live call establishes that a request falls outside what the catalog covers, apply the empty-results guidance in the main skill file and Rule 10 (never attribute a cohort figure to a named entity), and never substitute outside or training-data content.

## Discovery note

Use the connector's full catalogue listing for discovery and cache its result for the session; keyword search over data products is a spot-check. A library's live link comes from that keyword search result; a structured-data query returns no URL, so look the library up there when you need its link for a citation.

## Scope and vintage caveats

- A structured-data figure and a published-document figure for the "same" market can differ because of scope definitions (deployment categories, vendor inclusion), not error. Note it; do not treat one as wrong.
- Trackers release on a quarterly or semiannual cadence. When you compare a structured-data figure to a document figure, note both release dates.
