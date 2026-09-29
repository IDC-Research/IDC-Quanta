# Sourcing rules (route: sourcing)

Read on every sourcing request, alongside `references/rules.md`. These extend the twelve general rules, which still apply in full (Rule 3 citations, Rule 4 no drift, Rule 11 no fabricated inputs, Rule 12 external use). Where a sourcing file and `references/rules.md` differ on a general matter, `references/rules.md` wins. The sourcing header, wrapper exceptions and body shape are in `SKILL.md` and `references/sourcing/sourcing-core.md`.

## Tool scope — Tech Leader tools only

The sourcing route runs on the Tech Leader tools alone, in every package. Never call or search for document search, document download, Tracker or Spending Guide tools inside a sourcing engagement, and never read `references/mcp-playbook.md` or `references/idc-data-landscape.md`. The Tech Leader tools return no MarketScape title, URL or analyst name, so every sourcing citation is unlinked and no analyst is named. A question the Tech Leader tools cannot answer leaves the engagement (`SKILL.md`, Stay on the route).

## Rule 3a. Two source classes (extends Rule 3)

The Tech Leader tools front an unpublished dataset alongside MarketScape content. Citing dataset content to the MarketScape is a misattribution, because the document does not contain it. Decide the class before writing a Sources entry. (Class 2, published data products, belongs to the market intelligence route and is not used here.)

**Class 1, MarketScape content via Tech Leader:** `[n] IDC MarketScape assessment, <Market name> — via IDC Tech Leader`. Unlinked and without a year, because the tools return no title or URL. This is the no-URL form Rule 3 allows for sourcing: never construct or recall a MarketScape title or URL.

**Class 3, Tech Leader dataset.** Unpublished: no document, no title, no URL, so the entry is deliberately unlinked and carries no year. Two variants; cite only the ones used:

```
[n] IDC Tech Leader Vendor RFI, <Market name>, n = <X> vendors /
    <Y> product areas — unpublished IDC dataset, no subscriber document

[n] IDC Tech Leader Commercial Dataset, <Market name> — unpublished
    IDC dataset, no subscriber document[; list pricing dated per vendor,
    see inline]
```

- `<Market name>` is the display name set in stage 1 from the market record (scope intact), never an internal market identifier.
- `<X>` and `<Y>` are the market's distinct-vendor count and its product-area count, taken from the market taxonomy listing that publishes both separately. Never use one number for both, and never substitute a count of rating rows.
- Keep the trailing `— unpublished IDC dataset, no subscriber document` verbatim. Add the bracketed pricing clause only when the response shows list prices, and drop the brackets.

Numbering is positional across both classes, in order of first appearance. Never add an edition or period label to a table's source line.

**Which class a claim belongs to.** This matters most for the market-scoped vendor detail payload, which spans all three:

| Claim | Class |
|---|---|
| MarketScape tier (cross-checked per P0-1) | 1, MarketScape |
| Narrative overview, strengths, challenges, "consider when" prose | 1, MarketScape |
| Capability-coverage denominators, the MarketScape capability score, rating counts and histograms | 3, Vendor RFI |
| Requirement catalog rows, engine scores and ranks, the target company size | 3, Vendor RFI |
| Discount posture, volume sensitivity, value proposition, fiscal year-end, buyer-leverage and commercial bullets, competitive positioning | 3, Commercial Dataset |
| All list pricing and licensing, price ranges, price dates and deal counts | 3, Commercial Dataset |
| Vendor firmographics: annual revenue, founding year, funding type, associated companies | 3, Commercial Dataset |
| Capability-prose search hits | 3, Vendor RFI (directional; confirm before presenting) |
| A vendor's tiers in other markets, from its vendor-grain profile | 3, Vendor RFI |

**Class precedence, published outranks unpublished:** Class 1, then Class 3. State the published finding as the finding, then note any conflict in one line identifying the other side as unpublished dataset content. Never present the two as equally weighted, and never drop the published claim for the dataset.

**Pricing dates go inline, not in the Sources entry.** Price dates vary per product by years inside one market, so a market-level "as of" date would imply a stale price is current. Write it beside the figure, for example "$625/user/month (list, as of March 2026)", and flag any price over 16 months old as stale per Rule 9.

## Rule 8a. A coverage gap must be proven, never inferred from an empty result

An empty result is one of three things and only the third is a gap: the request was malformed, the entitlement is missing, or the data does not exist. Before reporting any gap, check both:

1. **The identifier came from a catalog, not from you.** Market names, vendor ids and filter values must have been read off a discovery call in this conversation, never typed from memory.
2. **The scope was widened once.** Try the parent market, the adjacent company-size cut, or the broader term within the Tech Leader catalog. There is no fallback to other IDC data.

A tool's own "no data available" wording is not proof. Treat it as a prompt to re-check the identifier. When a gap is real, say what is missing and at what grain.

## Cross-checks used across stages

- **P0-1. Tier cross-check.** Before printing any tier, compare the structured tier field with the tier stated in the vendor's narrative. On disagreement print the narrative tier, which is authoritative, with a one-line note that the structured field differs. Full handling in `references/sourcing/sourcing-selection.md`, stage 3 step 3.
- **P0-2. Completeness.** Enumerate the market's full vendor field from the market-filtered vendor catalog listing and account for every vendor not presented. Full handling in `references/sourcing/sourcing-selection.md`, stage 3.

## Provenance

- **P1.** Know where every requirement came from (RFI, conversation, or your inference) and be able to say so when asked. Do not print attribution in the stage 2 body. It surfaces in the requirement table's origin column where one exists, in the scoring-methodology brief, and in an export's methodology note.
- **P2.** Ground every tier, comparison and commercial claim in what the tools return, never memory, and cite it. Verified/Partial/Inferred is an internal test, never a printed label.
- **P2a.** Attribute by source class, not by tool. Route every claim from the market-scoped vendor detail payload through the Rule 3a table. A response presenting pricing or discount posture carries a Commercial Dataset entry; one presenting coverage denominators or engine scores carries a Vendor RFI entry.
- **P3.** Explain every shortlist change (promote, demote, drop) in plain prose: a hard-requirement miss, a tier, or a tech leader directive.
- **P4.** Where a change came from a tech leader directive, say so ("Per your direction…").
- **P5.** Cite MarketScape content in the unlinked Class 1 form. Never resolve or construct a MarketScape URL, and never hang dataset content off a MarketScape entry.

## Taxonomy

- **T1.** Tolerate loose naming (NetSuite → Oracle, "Singularity" → SentinelOne) and resolve every name to its canonical catalog entry before use. **The market, product-area and vendor identifier namespaces are distinct and the tools are strict about which they accept** — each tool's own description names the one it takes, so read it rather than assuming. Take an identifier from the catalog row the tool documents; a search-index id is a different kind of id and is rejected by the tools that want a catalog one.
- **T2.** Resolve the need to a single graded market and confirm it by name. Verify the hit matches intent: the real hazard is a plausible-but-wrong segment cut, where a market is genuinely the technology asked about but graded at a different company size. If no market fits, declare it unsupported.
- **T3.** Importance is tech-leader-owned and shape-tolerant: Critical / Medium / Nice-to-have, or prose. Never coerce a stance into a false numeric weight.

## Inference

- **I1.** A provisional market call is made out loud and confirmed before proceeding. Inferences are surfaced, never silently promoted to requirements.
- **I2.** Coverage gates drafting: where the Tech Leader catalog does not grade the market, there is no shortlist (Routing).
- **I2a. Check coverage depth, not just coverage.** The market taxonomy listing publishes the distinct-vendor count and the product-area count per market in one cheap call; read them before committing. Graded markets vary widely in depth, while the target shortlist is 5–8. Below roughly 8 graded vendors, say plainly the tech leader is seeing the market rather than a selection, and that this changes what the ranking means. Where the product-area count exceeds the vendor count, some vendors sell more than one product here, so decide up front whether the deliverable compares vendors or products, and say which.
- **I3.** Scoring is deterministic: prefer the scoring engine over hand-ranking, and use the tier the tool returns after the P0-1 cross-check. A change affecting a subset leaves the others' relative order undisturbed. Never freelance a ranking.
- **I3a. The engine scores every vendor, then removes those that fail a CRITICAL requirement.** A vendor failing a requirement set at CRITICAL is omitted from the returned ranking rather than returned with a zero score, unless it was protected (I3b). Partial satisfaction returns a fractional score and the vendor stays in. A low score means partial capability; an absence means a critical miss. So the returned set is the survivors, never the field: never describe the output as "the ranking of the market", and never report omitted vendors as dropped or missing. Enumerate the field separately (P0-2) and attribute every omission to the requirement it failed.
- **I3b. Exclusions and protections go to the engine; promotions are yours.** To exclude a vendor, pass it to the engine's discard list — a deterministic filter beats a hand-applied one, and a discard wins over a protection for the same vendor. **To keep a vendor in the ranking despite a critical miss, pass it to the engine's protect list.** That keeps the vendor from being removed; it does not lift its score or its position, so it is still ranked on its own merits. Use it where the tech leader wants a named vendor assessed anyway, and say plainly that it is present by their direction and where it actually landed. A promotion — moving a vendor above its computed score — is not something the engine does: apply it yourself after scoring, attributed, leaving the engine's relative order intact. Two disclosures whenever you present scored results: the engine breaks ties alphabetically, so re-order any tied block by capability coverage (descending) before any top-N cut and say the order within a tie is by coverage because the engine is indifferent; and scores are requirement-relative, so always show the coverage denominator beside the score.
- **I4. Persona separation.** Sourcing serves the buyer side. Seller-side work (winning a specific deal, battlecards, a vendor's competitive positioning, sizing a vendor's opportunity) belongs to the market intelligence route. Do not run both sides in one engagement, and never represent anything a technology leader shared as coming from or available to the vendor side. If a request appears to mix both, ask which side you are serving.

## Routing and escalation

- Market graded in Tech Leader → the sourcing route.
- Market graded but the requirement catalog genuinely errors → fall back to a tier-based read and say deterministic scoring is unavailable for that market. Do not pre-emptively degrade: requirement catalogs are normally available.
- Market not in Tech Leader → no fallback. Say IDC Tech Leader does not cover this market, so a scored shortlist is not available, and stop. Do not approximate one from capability-prose search, other IDC data or general knowledge.
- A question the Tech Leader tools do not answer (share trends, forecasts, IDC research on a vendor) → it leaves the engagement per `SKILL.md`, Stay on the route: answered at once on the market intelligence route in the Full package, or the fixed reply in the Tech Leader package. Never answer it under the sourcing header.
- Pricing or quote analysis beyond list price → out of scope; say so.
- Not an IDC question (chit-chat, coding, a non-IDC topic) → do not apply the wrapper, header, confidence or disclaimer to a non-IDC answer. Say briefly that it is outside IDC's coverage and offer to help with an IDC question instead.

## Voice and presentation

- **Never surface internal mechanics:** market ids, product-area ids, requirement ids, tool names or grounding tags. The tech leader sees market, vendor and requirement names and bracketed citations.
- **The workflow is method, never output.** See `references/sourcing/sourcing-core.md`.
- The general voice in `references/brand-voice.md` applies, except that sourcing responses use the body shape in `sourcing-core.md` (ledger, stage bodies, Recommendations) instead of the four-part Evidence / Implication / Watch body.

## Tier vintage and staleness

Tiers reflect a single company-size cut. Surface the **edition year** (where the Tech Leader data carries it) and the **target company size** in the shortlist and comparison output (in the table header, not the source line). Edition age alone is not a confidence downgrade: where the tier is the latest published edition, keep the response at its data-grounded confidence and state the year as a plain note. Note staleness per Rule 9, without pointing to other IDC data, and consider a downgrade only where the market is fast-moving and the cut is clearly out of date. Edition-over-edition tier change is not supported: resolve only to the current tier.

## Confidence for sourcing

A shortlist or comparison built from the market's own RFI ratings and the scoring engine rests on direct, on-point IDC data: rate it **High** by default. The market's MarketScape/RFI is definitive for that market, so relying on it alone is not a single-source downgrade. Downgrade only for a genuine defect in this answer: a data gap for the asked scope, a missing requirement catalog that forced a tier fallback, a tier conflict you could not resolve, requirements you had to assume because none were stated, a stated requirement you had to map to a looser catalog proxy, a headcount falling outside the graded cut's published band. A missing MarketScape link is never a downgrade.
