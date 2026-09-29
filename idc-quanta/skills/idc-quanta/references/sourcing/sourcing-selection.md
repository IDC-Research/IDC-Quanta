# Sourcing turn 2 — stages 3 and 4

Read on a proceed at checkpoint 1. Renders stages 3 and 4 only, then checkpoint 2. Do not build an RFP, a guide or any export on this turn.

**Stage 3 and stage 4 must not say the same thing twice.** Stage 3's per-vendor lines explain *why the vendor ranks where it does* against the stated requirements, plus its watch-out. Stage 4's table carries strengths, weaknesses and unique capabilities. Rank rationale belongs to stage 3, comparative assessment to stage 4.

## Stage 3 — My shortlist

**Workflow.**

1. **Score and rank deterministically** with the scoring engine, passing each requirement's priority and its qualifiers or numeric range where needed. Say so if asked whether the list is stable. **What it returns is the survivors, not the field (I3a):** the returned count tracks how strict the selection was, so read it against the graded field from stage 1 — a large gap means the requirement set is doing heavy filtering, and the tech leader sees that in the completeness line, not just the winners. A set of uniformly critical requirements also produces many equal top scores, leaving the score column with little to separate, so prefer a wider set at mixed priorities over a narrow all-critical one. If a market's catalog genuinely cannot be retrieved, fall back to the MarketScape tier and say plainly the ranking is tier-based, not scored.

   **Two disclosures on any scored output.** Show each vendor's capabilities-covered figure beside the score so a narrow-selection rank cannot be misread. And **break ties by coverage, not alphabet** — the engine orders a tied block alphabetically, so re-order it by capabilities covered (descending), apply that **before** any top-N cut so the cut is never decided by vendor name, and state that within a tie the order is by capabilities covered because the engine is indifferent. It only re-orders vendors the engine scored equally.

2. **Add evidence and a citation.** For every vendor you will present — not selectively — pull its tier and its narrative strengths and challenges from the market-scoped vendor detail, **and its vendor-grain profile**, passing the vendor and the market together. That profile is the source of annual revenue, funding type, founding year, associated companies and cross-market presence; a shortlist built on product-in-market detail alone cannot speak to whether the vendor will still be there in five years. Where a financial field comes back empty, write it as not disclosed rather than as zero, and never read an empty field as evidence that IDC holds no figure.

   **Passing the market alongside the vendor covers three things in one call:** the firmographics, this vendor's coverage denominator (so no separate ratings call is needed for the score column), and every market the vendor sells into **with its tier in each**. That per-market tier is a third, independent read — use it alongside the P0-1 cross-check below where a structured field and the narrative disagree.

   **The vendor detail also carries a MarketScape capability-axis score, on a 0–100 scale.** It is neither the requirement-match score nor the coverage denominator. Do not print it beside either without naming what it is, and never substitute it for the capabilities-covered figure.

   Route it: **viability into Watch-outs** (undisclosed revenue, sole-market presence or a small employee count are all material to a multi-year commitment); **cross-market presence into Rationale**, since a vendor holding strong positions in adjacent markets the tech leader also buys is a genuine consolidation argument. Funding type is the sharpest viability signal available — it distinguishes a public company from mature private ownership and from late- or early-stage venture backing. Carry the funding stage as returned rather than collapsing everything into "small vendor". Annual revenue arrives exact, banded, or unknown — reproduce a band as a band, never as a midpoint, and write an unknown as "not disclosed", never as zero and never silently omitted. Cite tier and narrative to the unlinked Class 1 MarketScape entry (P5).

3. **Run the cross-checks before printing any tier.** **P0-1:** the tier stated in the vendor's narrative is authoritative — print that. Where a structured tier field disagrees with it, the narrative still stands and the response's confidence is unaffected. Normalise casing for display rather than printing a tier in capitals. **Vendor-grain and product-grain reads can differ.** Where they conflict, the published MarketScape narrative is what the answer states, and the vendor record earns a one-line note flagged as unpublished (Rule 3a class precedence). Never a coin-flip between them.

4. **Apply tech leader overrides** as attributed, plainly-explained changes (P3/P4). Exclusions go to the engine's discard list and re-score. A vendor they want kept despite a critical miss goes to the engine's protect list, which holds it in the ranking without lifting its score. A promotion above a computed score is applied by you after scoring and labelled as such, never presented as the engine's output (I3b). Any override that moves a vendor against its computed score carries into the RFP's invited vendor set later, with its stated reason.

**Breadth and depth.** Present the strongest-ranked vendors — by default the Leaders plus the top-scoring Major Players, roughly 5–8, never more than 10. **One or two lines per vendor and no more:** why it ranks where it does against the stated requirements, its notable watch-out, and the bracketed number. Do not add a buy / evaluate / avoid verdict. Do not write a line inviting the tech leader to widen or trim the list — checkpoint 2 asks that already. Keep strengths, weaknesses and what each does that the others can't out of this stage.

**The body is exactly four things, in this order, and nothing else:** the shortlist table with its source line and one-line tier legend, the one-or-two-line block per vendor, the completeness line, and the italic methodology note as the final line. No preamble, no method, no export offer, no fifth element.

**The table first. No preamble.** Do not open with a sentence about how the scoring was done or which ratings were read — that is method, and method is never output.

```
**Your shortlist — <Market name> (IDC MarketScape <edition year, where the data carries it>, <target company size>)**

| Rank | Vendor | Product | Score | IDC MarketScape tier | Capabilities covered |
|---|---|---|---|---|---|
| 1 | Vendor A | Product A | 1.00 | Leader | 372/457 |
| 2 | Vendor B | Product B | 1.00 | Leader | 341/457 |
| 3 | Vendor C | Product C | 0.67 | Major Player | 298/457 |

Source: IDC MarketScape assessment, <Market name> — via IDC Tech Leader [1] · scores and coverage: IDC Tech Leader Vendor RFI [2]
```

Rank, vendor, product name, score and tier are all mandatory — a score alone does not tell a buyer what tier it sits inside. **State the edition year and the target company size in the table header** (`references/sourcing/rules-sourcing.md`, Tier vintage). Show the tier as text with a one-line legend naming the tiers in rank order (Leader, then Major Player, then Contender) and no colour words — the shortlist stays chat-only, so there is no export-time RAG or brand fill to apply. A per-vendor Source column carries the MarketScape's bracketed number only — never a number pointing at dataset content.

**Completeness (P0-2) — required, in this stage.** Enumerate the field from the market-filtered vendor catalog listing, which is complete and carries vendor names. Do not enumerate from the scoring engine, whose returned set is the survivors rather than the field, nor from the market record, whose product list carries product names rather than vendor names.

**Take both counts from the market taxonomy listing, which publishes the distinct-vendor count and the product-area count separately (Rule 3a).** Use the vendor catalog listing for the names and the roster. State how many vendors and how many product areas the market grades, and **account for every vendor you are not presenting**, phrased as what it is: "*N* vendors did not meet one or more of your hard requirements", naming them and, where you can, the requirement that excluded them. Keep the two kinds of omission separate — engine-filtered vendors in that line, vendors *you* removed under a must-NOT-have in their own sentence naming the exclusion. **Attributing an omission is one cheap call:** re-run the scoring with the suspect requirement alone and see whether the vendor survives; absent means that requirement excluded it. Probe on demand for the vendors a tech leader asks about rather than pre-computing all of them. Never write that vendors were dropped, missing, or lost to a data defect — that tells a tech leader a credible option does not exist when their own criteria excluded it. If a named vendor they expect is absent, say which requirement removed it and offer to relax it and re-score.

**A requirement that collapses the list is surfaced, never applied silently.** If the set leaves one vendor or none, do not present that as the shortlist. Name the limiting requirement and offer the three ways out: "Adding [requirement] leaves only [count] vendor(s) on your shortlist. Want to keep it, relax it, or try [alternative] instead?".

**Close the stage with the methodology note, in italics, as the last line of the body:**

```
*For a brief on how these scores were derived, type "Details on Scoring Methodology".*
```

That one line, business-formal. Not optional, not a Recommendations item. `references/sourcing/scoring-methodology.md` defines what to produce when asked, by that phrase or any free-form version of it.

**Do not offer an export here.** The shortlist is never a file — this skill only exports the RFP and the negotiation guide, both from the turn-3 menu (`references/sourcing/exports/common.md`). If a tech leader asks for the shortlist itself as a spreadsheet, say plainly that isn't something this skill produces.

### Mode: alternatives beyond incumbents

Trigger: "emerging or alternative vendors", "who else besides [incumbents]", "options beyond our current shortlist."

Run stages 1–3 with two changes. First, capture the incumbent set and exclude it in the scoring step through the engine's discard list, so the ranking surfaces the field *minus* the incumbents. Deprioritising is not available — either discard outright, or leave the vendor scored and reorder it yourself as an attributed change (I3b). Second, highlight the strongest non-incumbents, especially Major Players or Contenders that score well, as candidates worth adding, with the same evidence and citation as any shortlisted vendor. Mark which vendors are incumbents in the table.

**Honesty note:** "gaining momentum", "fastest-growing" and "peer adoption" are time-series and installed-base signals these tools do not carry. Say so plainly rather than inferring a growth trend from structured vendor data. Do not offer to pull Tracker or research data inside the engagement.

## Stage 4 — Comparison

**Always runs in the same turn as stage 3, and is produced rather than offered.** The tech leader never asks for it and is never asked which vendors to compare — checkpoint 2 asks whether they want vendors *added to the assessment*, a different question answered after both stages are on the page. **The compared set is the top three to five from the shortlist, chosen by you:** top three by default, four or five where the scores are close enough that the cut would be arbitrary. Where fewer than three survived, compare all of them and say so. Do not skip this stage because the response is getting long — if length is tight, shorten stage 3's rationale.

Where the tech leader arrived directly with a named set, stages 2 and 3 are Skipped and stage 1 still runs: resolve the market from the named vendors and confirm it by name.

**Workflow.**

1. **Take the compared set, then resolve it if needed.** By default it is the shortlist's top three, already resolved in stage 3. Only where the tech leader named the vendors do you resolve each name (T1). Where they name a **product** rather than a vendor, resolve it through product search, which also returns every market that product sells into — then two checks before accepting a hit: confirm the returned market is the one under discussion, since a real product can resolve into an adjacent market, and treat an implausible result as an unresolved name rather than an answer. On either, fall back to the vendor behind the name. Where the vendor count and the product-area count diverge, at least one vendor sells several products here, which decides whether the columns are vendors or products (I2a).

2. **Pull per-vendor detail at both grains** — tier, narrative strengths and challenges and list pricing from the product-in-market detail, **and the vendor-grain profile** for annual revenue, funding type, founding year, associated companies and cross-market presence. Viability belongs in a comparison as much as capability: a vendor with undisclosed revenue or a single-market footprint is a different proposition from a $1B vendor holding positions in eight markets, and a criteria matrix will never show it. Where a vendor has more than one product in the market, compare products, not vendors, and say which product each column is. Where the grains conflict, the MarketScape narrative is what the answer states and the vendor record earns a one-line note flagged as unpublished.

3. **Derive strengths, weaknesses and unique capabilities from data you already hold.** Strengths and weaknesses come from the narrative pulled in step 2, condensed to the two or three that matter for *this* tech leader's requirements, not the full narrative. **Unique capabilities are computed where the ratings allow and named honestly where they don't.** Preferred method: compare the capability ratings across the compared set and keep only what one vendor fully supports and the rest do not — these are the ratings pulled at intake and reused for stage 3's denominators, so in the normal case this needs **no additional call**. Where what you hold does not settle it, either make one paged ratings call for the compared set, or fall back to the differentiator lines in the narratives **and say the read is narrative-derived**. Uniqueness is relative to this group, not the market; say so once. Where nothing differentiates a vendor within the group, write "nothing unique within this group" — a real and useful finding. **The cost of this column is never a reason to skip the stage.**

4. **Criteria matrix on request only.** It is a second, wider table that does not fit the paced body, so stated criteria alone do not trigger it. When asked, ground the criteria in the requirement catalog and pull per-element ratings for a deterministic matrix rather than an inferred one. Filter to the elements the criteria cover, or for a broad comparison group by axis and surface only where vendors differ. Every partial or unsupported cell is marked, never blank. Present it beneath the concise table, never instead of it.

5. **Cost view on request.** Surface real per-edition list pricing with its own date and say it is list pricing, not a TCO benchmark. Pricing is Class 3 Commercial Dataset content: add that Sources entry, keep each date inline beside its figure, and never cite a price to the MarketScape.

6. **Honest gaps.** Peer-experience and SLA benchmarking, and analyst-coverage trajectory over time, are not available from these tools — say so rather than inferring. Capability-prose search does not close this gap and must not be used to: it is not scoped to a market, so any hit must be confirmed against the market in question before it is presented.

**Presentation — the concise comparison table. One row per vendor**, in shortlist rank order; columns are **Strengths**, **Weaknesses** and **Unique capabilities**. Deliberately short — a few phrases per cell, never paragraphs.

```
**Comparison — your top <N>**

| Vendor | Strengths | Weaknesses | Unique capabilities |
|---|---|---|---|
| Vendor A | Breadth across source-to-pay; strong midmarket references | Premium pricing; heaviest implementation | Native supplier risk scoring |
| Vendor B | Deep invoice capture; EMEA compliance coverage | Thinner payments functionality | Statutory e-invoicing in 14 EMEA markets |
| Vendor C | Fast deployment; genuinely ERP-agnostic | Smaller North American partner network | Nothing unique within this group |

Source: IDC MarketScape assessment, <Market name> — via IDC Tech Leader [1] · capability ratings: IDC Tech Leader Vendor RFI [2]
```

Vendors are the rows and those three are the columns. Do not transpose it and do not add a fourth column.

**Beneath it, a one-line attribute block per vendor** carrying the **IDC MarketScape tier** spelled out (never a bare "Tier"), the MarketScape **edition year** where the Tech Leader data carries it, the IDC capability score **with its capabilities-covered figure**, and the target company size. Cite by source class: tier, strengths and weaknesses to the MarketScape; the capability score, the coverage figure and the unique-capability read to the Vendor RFI entry. Vendor and market **names** only, never internal ids.

### Mode: architecture and strategic-fit comparison

Trigger: "architectural alignment", "strategic fit", "integration / interoperability", "lock-in risk."

Run stage 4 above, including its criteria-matrix rule, which still needs an explicit request. Where a matrix is asked for, build the criteria axis from the market's architecture- and integration-related requirement elements (deployment model, platform support, integration, portfolio breadth) and pull each vendor's per-element ratings for those. Draw the strategic-direction read from the vendor-detail narrative. Where the tech leader states weighted architecture criteria, the scoring engine can produce an alignment ranking against them.

**Lock-in and portfolio breadth are measured, not inferred.** The vendor-grain profile is the evidence: it lists every market the vendor sells into with its tier in each, so breadth is a count and consolidation exposure is a named list rather than an impression from prose. Read it alongside the **product**-grain cross-market view, which answers a sharper question — how far the *specific product* under evaluation reaches. Microsoft Dynamics 365 alone spans five markets, so a tech leader standardising on it consolidates far more than ERP, whereas a vendor can be broad while the product in front of them is narrow. Read it both ways: breadth as an argument *for* the vendor where the adjacent markets are ones the tech leader also buys, concentration as lock-in risk where standardising would span many of their categories at once. Then flag the interoperability concerns and architectural lock-in risks the narrative surfaces on top of it.

**Honesty note:** forward roadmap trajectory is limited to what the narrative and product-strategy fields carry. A genuine multi-year trajectory read is outside what these tools carry: state the gap.
