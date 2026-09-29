# Sourcing turn 1 — stages 1 and 2

Read when the intake answers come back. Renders stages 1 and 2 only, then checkpoint 1. Do not score a shortlist or pull vendor detail on this turn, apart from the single naming read in stage 1 step 4.

## Stage 1 — Market identification

**Workflow.**

1. **Resolve and confirm the market.** Resolve the need to a single IDC market and confirm it by name before anything else. Ask the market search to enrich its rows with market context, so each candidate's description arrives on the search row — that is the cheapest way to tell adjacent cuts apart, and it replaces a separate market lookup per candidate. Verify the hit matches intent. **The real hazard is a plausible-but-wrong segment cut:** adjacent markets are both genuinely the technology asked about but graded at different company sizes. Confirm the scope, not just the topic (T2).

   **Where the tech leader's own headcount falls outside every graded cut, or between two of them, disclose it and proceed — do not stop to ask.** Work in the cut they stated, or the nearer band where they stated none; name the cut you are working in, name the band it covers, say plainly that their headcount sits outside or between the published bands, and name the adjacent cut as available. Carry the mismatch into the confidence line. A headcount between two bands is a disclosed limitation on the answer, never a blocker to producing one, and the only case that stops the engagement is no defensible cut at all. If no market fits, or the market is not in the Tech Leader catalog, say IDC Tech Leader does not cover it and stop (`references/sourcing/rules-sourcing.md`, Routing).

2. **Check depth before drafting.** Read the distinct-vendor count and the product-area count from the market taxonomy listing — one cheap call that decides three things: whether the market is deep enough that a shortlist is a real selection, whether the deliverable compares vendors or products when the counts diverge, and the `n = X vendors / Y product areas` figure the Class 3 citation needs. Where two candidate markets are both plausible, the same call lists them side by side with their counts. Do **not** use category search here: it omits the vendor count and returns every market's full vendor roster.

3. **Where the stated need maps to no single market**, capability-prose search is the discovery aid — it searches vendor prose across the whole corpus and its hits point at the market that owns the capability (a shop-floor-control need surfaces Manufacturing Execution Systems, not ERP). Use it to *find* the market, never to populate a shortlist: it cannot be scoped to a market, so confirm the market before relying on any hit.

4. **Name the market from the market record, then the MarketScape reference.** Read the chosen market's own record for its description. The display name is the catalog name plus the company-size, regional or industry scope, because that scope is the part a tech leader needs and the bare catalog name usually drops it. **The market record often states no scope.** Where it doesn't, read one vendor detail in the market (the first graded product is enough): its narrative names the backing MarketScape, for example "the 2024 IDC MarketScape for worldwide modern endpoint security for midsize businesses". Take the scope and the edition year from that sentence, so this market is **Endpoint Security for Midsize Businesses**, never bare "Endpoint Security". This one call is preparation for naming the market, not a vendor pull. Add an employee band only where the data publishes one, and never invent one. Where neither source states a scope, use the catalog name as is.

5. **Keep the candidate list.** Record every market the search surfaced as plausible and which was chosen. The passed-over block and the scoring-methodology brief both need it, and it is not recoverable later without re-running the search. Carry it forward across turns.

6. **Then ask the intake questions, and render nothing else that turn.** On any first request for a selection, everything above is preparation for the card, not output. Per `references/sourcing/questionnaire.md`, pull the requirement catalog and the market's per-element vendor ratings on the same turn — the ratings are what let you pick reference criteria that actually split the field — then call the question tool and stop.

**Presentation. Exactly two things, in this order. Nothing before, between or after them.**

**1. The market name and its definition — one sentence.** The name as set in step 4, scope intact, then one sentence of definition from the market record carrying its bracketed citation. One sentence: not two, not a sentence plus a clarifying clause.

```
**Endpoint Security for Midsize Businesses (100–2,499 employees)** — endpoint prevention, detection
and response for a segment where vendors target subsegments rather than build one generalised
platform [1].
```

The definition always carries a citation to the Class 3 Vendor RFI entry for the market. Never leave it uncited.

**2. Considered and passed over — a bare list of names.** Up to five, five the hard maximum. **Names only:** no definitions, no reason anything was passed over, no follow-up.

```
**Considered and passed over**

- B2B Revenue and Profit Optimization
- Retail Marketplace Platforms Software Providers
- Retail Demand Planning and Forecasting
```

Omit the block entirely when nothing else was plausible. Never write a line explaining there were no alternatives, and never manufacture candidates to fill it.

**What does not go in this stage:** graded depth or vendor counts (stage 3's completeness line is the only place that figure is used), edition-year narrative (the year goes in the stage 3 table header), any statement that a check found nothing, a restatement of the requirements, or commentary on the taxonomy.


## Stage 2 — My requirements

**Workflow.**

1. **Capture requirements with importance and attribution.** Critical / Medium / Nice-to-have, plus any must-NOT-have capabilities, each attributed to where it came from — RFI, the conversation, or your inference (P1, known but not printed in this body). Inferences are surfaced, never silently promoted (I1).

2. **Ground them in the market's requirement catalog** so they map to real IDC-defined criteria rather than free-form prose. Catalogs can run to more than 100 requirements. **Go straight to full rows for any catalog under roughly 60 requirements** — summary mode suppresses the classification, the requirement type, the qualifier list and the observed numeric range, which are exactly what a scoring payload needs, so browsing first costs a round trip and saves nothing. Use summary only to skim a genuinely large catalog. **Each row publishes its own classification — functional, technical or company — so a mapped requirement is classified by IDC's taxonomy rather than your judgement.** Fall back to your own judgement only for requirements the catalog does not carry. Say nothing about this in the response; it is a correctness rule, not a disclosure.

3. **Sort for presentation** into functional, technical and company, and within each, critical vs non-critical. This is the tech leader's own view and it is what the table shows — keep it distinct from the engine priorities, which are what get scored. Critical maps to critical; Medium and Nice-to-have to non-critical.

4. **Where the tech leader gave no requirements**, do not fabricate any and do not score around the gap. The intake card fills this stage, so it runs *after* the answers come back. Requirements picked from the card are already catalog rows and go to the engine at CRITICAL directly. Anything added as free text is mapped where a row exists and marked unscored where none does. If they skipped the requirements questions, proceed on the market's most heavily weighted catalog criteria, mark the requirements assumed rather than stated, and carry that and the assumptions into the **confidence line**, not this body. **A table reading "None stated" across all three rows means this stage never ran** — go back and ask rather than presenting an unscored shortlist as a selection.

5. **Where requirements arrived in an upload**, parse it, let it pre-answer the card, and ask only for confirmation plus what is genuinely missing. Keep the tech leader's content and IDC's visibly separate, and never treat uploaded content as IDC data (Rule 4). On an upload failure, follow the branches in `references/sourcing/questionnaire.md`: say what happened, offer the way forward, and never mark this stage Completed.

**Numerical requirements: choose thresholds inside the published range.** A numerical row carries the observed minimum and maximum — what the market's vendors actually reported. A window spanning well beyond that range scores every vendor identically and tells you nothing, so place the bound where it separates the vendors you want from the ones you don't. Where the observed range is empty, no vendor has a usable value and scoring that row cannot discriminate at all — leave it out. **Where you had to interpret a qualitative ask ("deep partner network", "high satisfaction") as a number, that threshold is your inference:** disclose it in the confidence line and carry it into the export's requirements sheet, never present it as the tech leader's own figure.

**Must-NOT-have requirements: look for a catalog requirement that states the absence before falling back to a manual exclusion.** The engine has no negation operator — you cannot negate a positive requirement — but catalogs themselves carry some requirements already phrased as an absence, and those score like any other (Endpoint Security publishes "The DVM solution does not require additional software agent to be deployed and enabled"). So search the catalog for the exclusion first, by the capability it names and by words like *does not require*, *without*, *agentless*, *no additional*. If one exists, **pass it to the engine at CRITICAL** — a deterministic filter beats a hand-applied one. Say in the response that the exclusion was scored, not hand-applied.

**When the catalog carries no such requirement, enforce it yourself after scoring.** Three steps. First, keep the exclusion out of the scoring payload: never invent an inversion (a stated "must not have DLP" is not a "must have DLP" requirement) and never pass the bare capability it names as a proxy, which scores the opposite of what was asked. Second, after the engine returns survivors, check each against the exclusion using the capability ratings or the vendor narrative and **drop every vendor that violates it** — a stated must-not-have is as hard as a CRITICAL requirement. Third, disclose both the exclusion and the drops in stage 3's completeness line, as failing a stated exclusion rather than folded into the generic wording, and say in one line that it was applied after scoring rather than by the engine. Where the ratings do not settle whether a vendor violates it, say the evidence is inconclusive and keep the vendor in with the open question flagged — never drop a vendor on an inference (I1).

**Presentation — the table, and only the table.** Rows are the three requirement types, columns critical and non-critical. Short phrases per cell.

```
**Your requirements**

| | Critical | Non-critical |
|---|---|---|
| Functional | Three-way invoice match; partial payments | Supplier self-service portal |
| Technical | SOC 2 Type II; native NetSuite connector | Open API for custom workflows |
| Company | Midmarket install base in EMEA | Named CSM |
```

**Write nothing after the table.** It is the tech leader's own content, not an IDC figure, so it carries no source line under Rule 3. No attribution paragraph, no note on where requirements came from, no explanation of how they were sorted. The only permitted additions live inside the cells: mark a requirement with no catalog match as "not in IDC's requirement catalog — not scored", and write "None stated" in a cell the tech leader left empty rather than inventing content.

The table is a **categorisation of what the tech leader wrote**, so every requirement they gave appears in it. Never present IDC's catalog criteria as though they were the tech leader's; where the card was skipped and you scored on catalog weighting, the cells say so.
