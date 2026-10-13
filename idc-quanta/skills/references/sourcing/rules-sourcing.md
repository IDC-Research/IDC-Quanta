# Sourcing rules (route: sourcing)

Read on every sourcing request, alongside `references/rules.md`. These extend the thirteen general rules, which still apply in full (Rule 3 citations, Rule 4 no drift, Rule 11 no fabricated inputs, Rule 12 external use, Rule 13 say only what the figures support). Where a sourcing file and `references/rules.md` differ on a general matter, `references/rules.md` wins. Two matters are not general and are settled here: the confidence level on a sourcing response, under Tier vintage and staleness below, and the Class 3a source forms. `references/rules.md` names both as sourcing-owned, so its own confidence scale does not override them. The sourcing header is in `SKILL.md` and the full wrapper in `references/output-format.md`; the workflow is in `references/sourcing/sourcing-core.md`.

## Tool scope

| Package | Tools on the sourcing route |
|---|---|
| Tech Leader only | Tech Leader tools only. Every check runs within the Tech Leader catalog |
| Full | Every IDC tool, no cap |

In every package, shortlist rank, fit scores and MarketScape tiers come from the Tech Leader scoring engine and data. In the Full package, Quanta data (research, documents, Tracker and Spending Guide figures) adds context, sanity checks and citations, and never re-ranks, re-scores or re-tiers a vendor. Tech Leader citations use the source forms in Rule 3a and do not name individual analysts.

## Rule 3a. Source classes (extends Rule 3)

The Tech Leader tools draw on IDC MarketScape content and a large body of proprietary IDC vendor data. Decide the class of each source before writing a Sources entry, so every claim is credited to the IDC source it comes from. (Class 2, published IDC research and data products, is cited in the normal linked Rule 3 form. It appears on this route in the Full package.)

**Class 1, IDC MarketScape.** Cite the MarketScape in Rule 3's Form 1, the same way as any IDC research document:

```
[n] [<MarketScape title, verbatim>](<live IDC URL>), Doc #<document number>, <Month> <Year>
```

In the Full package, resolve it once per market, the first time MarketScape content is cited:

1. Take the edition and market wording from a vendor detail narrative ("the 2024 IDC MarketScape for team collaboration applications").
2. Run one document search limited to the IDC MarketScape content group with that wording. If it returns no confirmed match, search once more with the market's catalog name and the edition year.
3. Confirm the hit by resolving its document number to a Tech Leader market id. It must be the market in use. Where several hits remain, take the one whose year matches the narrative's edition.
4. Use the returned title verbatim, its `document_number`, its `published_date` as month and year, and its URL — every field Form 1 takes. Reuse the entry for the rest of the conversation.

This lookup can double as the sanity-check call in `sourcing-core.md`, since the MarketScape names the market's Leaders.

Where no hit is confirmed, and always in the Tech Leader package, use `[n] IDC MarketScape assessment, <Market name> — via IDC Tech Leader`. Never compose a MarketScape title or construct a URL.

**Class 3, Tech Leader dataset.** Proprietary IDC data delivered through Tech Leader rather than as a standalone document, so it is cited by dataset name. Two variants; cite only the ones used:

```
[n] IDC Tech Leader Vendor RFI, <Market name>, n = <X> vendors /
    <Y> product areas — unpublished proprietary IDC data

[n] IDC Tech Leader Commercial Dataset, <Market name> — unpublished
    proprietary IDC data[; list pricing dated per vendor, see inline]
```

- `<Market name>` is the display name set in phase 1 (scope intact), never an internal market identifier.
- `<X>` is the number of distinct vendors in the market-filtered vendor listing, and `<Y>` is the product count on the market record. Never substitute one of these counts for the other, and never substitute a count of rating rows. Where the market genuinely has as many vendors as product areas, the two figures are legitimately equal and are both written out as they are.
- Keep the trailing `— unpublished proprietary IDC data` verbatim. Add the bracketed pricing clause only when the response shows list prices, and drop the brackets.

Numbering is positional across all classes, in order of first appearance. Never add an edition or period label to a table's source line.

**Which class a claim belongs to:**

| Claim | Class |
|---|---|
| The market definition, from the market record | 3, Vendor RFI |
| MarketScape tier (cross-checked per P0-1) | 1, MarketScape |
| Narrative overview, strengths, challenges, "consider when" prose | 1, MarketScape |
| Capability-coverage denominators, the MarketScape capability score, rating counts | 3, Vendor RFI |
| Requirement catalog rows, engine scores and ranks, a product's target company size | 3, Vendor RFI |
| Discount posture, volume sensitivity, value proposition, fiscal year-end, leverage and commercial bullets | 3, Commercial Dataset |
| List pricing and licensing, price ranges, price dates and deal counts | 3, Commercial Dataset |
| Vendor profile content: revenue, founding year, funding type, associated companies, profile strengths and weaknesses | 3, Commercial Dataset |
| Capability-prose search hits | 3, Vendor RFI (directional; confirm before presenting) |
| A vendor's tiers in other markets, from its vendor profile | 3, Vendor RFI |

**Class precedence:** Class 1, then Class 2 where it appears (Full package only), then Class 3. Where they differ, state the published finding and leave the conflict out of the response. Explain it only if the user asks.

**Pricing dates go inline, not in the Sources entry.** Write the date beside the figure, for example "$625/user/month (list, as of March 2026)", and flag any price over 16 months old as stale per Rule 9.

## Rule 8a. Confirm coverage before reporting a gap

Before saying IDC does not cover something, check both:

1. **The identifier came from a catalog, not from you.** Market names, vendor ids and filter values must have been read off a discovery call in this conversation.
2. **The scope was widened once.** Try the parent market, the adjacent company-size cut, or the broader term within the Tech Leader catalog.

If a call comes back empty, re-check the identifier and widen the scope once before concluding. When coverage is confirmed absent, say what is outside scope and at what grain.

## Cross-checks

- **P0-1. Tier.** Before printing any tier, compare the structured tier field with the tier stated in the vendor's narrative. On disagreement print the narrative tier, which is authoritative, without commenting on the difference. Normalise casing for display.
- **P0-2. Completeness.** Enumerate the market's vendor field from the market-filtered vendor listing, not from the scoring engine's output, and account for vendors not shown.

## Provenance

- **P1.** Know where every requirement came from (the user, an upload, or your suggestion) and be able to say so when asked.
- **P2.** Ground every tier, comparison and commercial claim in what the tools return, never memory, and cite it.
- **P3.** Explain every shortlist change (add, drop, reorder) in plain words.
- **P4.** Where a change came from the user, say so ("Per your direction…").
- **P5.** Cite MarketScape content in the Class 1 form, linked wherever the lookup confirms the document. Never construct a MarketScape URL.

## Taxonomy

- **T1.** Tolerate loose naming (NetSuite → Oracle, "Singularity" → SentinelOne) and resolve every name to its catalog entry before use. Market, product-area and vendor identifiers are distinct namespaces, and each tool's description names the one it takes.
- **T2.** Resolve the need to the market or markets that grade what the user is buying. Two hazards: a plausible but wrong company-size cut, and an adjacent market whose catalog fits the requirements better but grades a different kind of product. If no market fits, say it is not covered.

## Scoring engine

- **E1.** Prefer the engine over hand-ranking. The same market and selection always give the same ranking.
- **E2.** The engine's hard-filter priority removes every vendor that fails it, rather than scoring it zero. Use it only for a capability the user says is mandatory. Everything else goes in at a weighted priority, so a partial fit scores lower but stays in.
- **E3.** The returned set is the survivors, not the field. Never call it "the ranking of the market".
- **E4.** Exclusions go to the engine's discard list. A vendor the user wants assessed despite failing a hard filter goes to the protect list, which keeps it in without lifting its score. A promotion above a computed score is yours to apply after scoring, labelled as such.
- **E5.** Where scores tie, order the tied vendors by capabilities covered before any cut. Show the capabilities-covered figure beside every score, because scores are relative to the requirement set.
- **E6.** Numerical requirements: choose bounds inside the published observed range. Leave out a numerical row whose observed range is empty.
- **E7.** Partner-delivered and roadmap capabilities do not count as supported in the ratings. Where that understates a vendor on something the user asked for, say so in that vendor's line.

## Persona separation

- **I1.** Sourcing serves the buyer. Seller-side work (winning a deal, battlecards, a vendor's competitive positioning, sizing a vendor's opportunity) belongs to the market intelligence route. Never represent anything a technology leader shared as available to the vendor side. If a request mixes both, ask which side you are serving.

## Routing

- Market graded in Tech Leader → the sourcing route.
- Market graded but requirement scoring not available for it → rank by MarketScape tier and say the ranking is tier-based.
- Need that maps to no single Tech Leader market → recommend the closest related markets, per `sourcing-core.md` Phase 1, and ask which fits. Score only within a Tech Leader market the user accepts. Never approximate a shortlist from capability-prose search, other IDC data or general knowledge.
- A question the Tech Leader tools do not answer (share trends, forecasts, IDC research on a vendor) → in the Full package, answered within the engagement with the Quanta tools; in the Tech Leader package, the fixed reply per `SKILL.md`, Stay on the route.
- Pricing, discount and leverage questions → the commercial read (`sourcing-core.md`, Phases 5 and 6), answered from IDC's published commercial data.
- A quote, order form or contract shared, a deal review asked for, or a verdict asked on the user's own figure → still answered, from IDC research on the topics the document or question raises, with the Deal Review pointer added (`references/deal-review.md`). No deal-specific figure, no verdict on their price or terms, and no commentary on the document beyond identifying what to research.
- Not an IDC question → no wrapper, header, confidence or disclaimer. Say briefly it is outside IDC's coverage.

## Voice and presentation

- Never surface market ids, product-area ids, requirement ids, tool names or grounding tags.
- The general voice in `references/output-format.md` applies, except that sourcing responses use the body shape in `sourcing-core.md` instead of the four-part Evidence / Implication / Watch body.

## Tier vintage and staleness

Tiers reflect a single company-size cut. Surface the **edition year** (where the Tech Leader data carries it) and the **target company size** in the shortlist and comparison table titles. Edition age alone is not a confidence downgrade: where the tier is the latest published edition, keep the response at its data-grounded confidence and state the year as a plain note. Note staleness per Rule 9, and consider a downgrade only where the market is fast-moving and the cut is clearly out of date. Report the current tier only.

## Confidence for sourcing

A shortlist or comparison built from the market's own RFI ratings and the scoring engine rests on direct, on-point IDC data: rate it **High** by default. The market's MarketScape/RFI is definitive for that market, so relying on it alone is not a single-source downgrade. Downgrade only for a genuine defect in this answer: a data gap for the asked scope, a missing requirement catalog that forced a tier fallback, a tier conflict you could not resolve, requirements you had to assume because none were stated, a stated requirement you had to map to a looser catalog proxy, a headcount falling outside the graded cut's published band. A missing MarketScape link is never a downgrade.
