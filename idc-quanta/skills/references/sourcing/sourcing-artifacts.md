# Sourcing turn 3 — the menu, and stages 5 and 6

Read on a proceed at checkpoint 2, or when the tech leader asks about pricing, leverage or an RFP directly. Turn 3's body shape is in `references/sourcing/sourcing-core.md`. File specs are in `references/sourcing/exports/`.

## Checkpoint 3 — the artifact menu

Mandatory: every full engagement reaches it, so the RFP and negotiation preparation are always put in front of the tech leader. Business-formal wording — full sentences, no contractions in the descriptions, no sales language. Present through the question tool, after the message.

```
questions: [
  { header: "Deliverable", multiSelect: false,
    question: "Which would you like me to produce?",
    options: [
      { label: "Build the RFP",
        description: "A formal request for proposal carrying your confirmed market, requirements and invited vendors, plus a companion response template for vendors to complete. Available as a short form or the full formal long form." },
      { label: "Prepare for negotiation",
        description: "A commercial briefing on the vendors you take forward: discount posture, volume sensitivity, list pricing to anchor against, and where your leverage sits. Deliverable here or as a guide you can forward." } ] } ]
```

Where they pick both, or name both in free text, build them in the order they asked. Then run that artifact's stage: stage 5 for the RFP, stage 6 for negotiation preparation. These two are the only files this skill exports — the shortlist and the comparison stay chat-only, per `references/sourcing/exports/common.md`.

## Stage 5 — Build the RFP

**Runs only when picked from the menu or asked for directly.** It renders no body before that — no offer, no preview, no placeholder. The menu's description stands in for an offer. An RFP leaves IDC's platform and reaches vendors, so it is never generated speculatively and never silently reissued.

**Workflow.**

1. **Capture the RFP-specific asks in one go** — **which shape** (a short lightweight RFP or the full formal long form; offer the lightweight one where nothing indicates a preference), the proposal due date, the submission contact, questions cut-off, any mandated section order, evaluation weighting, their own template if they have one, and any commercial terms to state up front. Ask once for what is missing and material; do not interrogate. Both shapes are specified in `references/sourcing/exports/rfp.md`.
2. **Build from the standing stages 1–3 without re-asking for any of them.** The confirmed market, the requirements table (including every requirement marked "not in IDC's requirement catalog") and the approved shortlist carry straight through. Re-asking for a requirement the tech leader already gave is a defect, not diligence. Any catalog requirement they never discussed or prioritized is surfaced here too — ask whether to include it at a lower default priority, leave it open for vendors, or drop it — and any stated need with no exact catalog match, only a generic proxy, is named as a substitution rather than silently equated.
3. **Use their supplied template if one exists; otherwise IDC's default structure** — and state in the document itself which was used.
4. **Validate the evaluation-criteria weightings sum to 100% before generating.** If they don't, flag the discrepancy and ask how to close the gap rather than generating a document with a broken table.
5. **State every assumption and list every placeholder in the document**, not only in chat: the vendor receiving it needs the same clarity a returning tech leader would. Placeholders are enumerated in one place so nothing ships half-filled, and a placeholder is written as an obvious placeholder, never as plausible invented content.
6. **Produce the vendor response template alongside it**, structured on the same requirements, with the three-state response schema `references/sourcing/exports/rfp.md` specifies.
7. **Cite.** The requirements ranking that shaped the RFP carries a citation appendix, and the citations survive into the file rather than living only in chat.
8. **Never overwrite a prior RFP.** If requirements or the market change afterwards, say the previous version may already be with vendors, mark the stage Outstanding again, and rebuild only on an explicit instruction.

**Presentation in chat, once built.** Short: a line naming the shape built and the template used, the list of the tech leader's stated asks (due date, contact, weighting, anything else), which sections came directly from the tech leader versus what stays their own responsibility from here (vendor Q&A, references, negotiating a best and final offer), a one-line statement of how many assumptions and placeholders the document flags, and the download link. Before the artifact is picked, the stage has no body at all.

## Stage 6 — Negotiation preparation

**Runs when picked from the menu, or when the tech leader asks about pricing, discounting, leverage or terms at any point** — whatever turn that lands on. Where they pick it, ask which vendors they are taking forward. Ask the tech leader only for what only they know — their own budget ceiling, their contract's renewal or end date, other vendors seriously in play, who will be in the room — never for anything about a vendor's own business the tools should supply instead (fiscal year-end, discount posture, funding stability). Where more than one person will represent their organization, offer a separate, personalized guide per named persona rather than one generic version, built from the same underlying vendor facts so the set stays consistent. Then produce the commercial read and mark the stage `Completed`.

Two halves. The **commercial read** is produced in chat whenever they ask. The **negotiation guide** is a document and follows the stage-5 rule: only on explicit go-ahead.

**Workflow — the commercial read.**

1. **Leverage and discount posture.** Per vendor, pull the commercial-insights payload: the buyer-strength and negotiation-leverage points, discount ranges and rationale, volume sensitivity. Present the leverage points as IDC's analyst-authored guidance and cite them to the **Commercial Dataset** entry — the whole payload is Class 3, unpublished and unlinked, so it never cites to a MarketScape URL, and it is qualitative guidance rather than hard figures. **Absent-data branch:** IDC commercial data covers some vendors and not others. Where it is absent, say plainly there is no IDC commercial data for that vendor rather than implying no leverage, and lean on step 3.
2. **List pricing to anchor against.** Pull real per-edition list pricing with its own date — the firmest number in the stage, stated with that date. It is a single vendor's list price, not a cross-market benchmark; say so. **Dates are per product and can span several years inside one market**, so never imply a single "as of" date for a market's pricing, put each date inline beside its own figure, and flag any price over roughly 16 months old as stale before a buyer anchors on it. Where a product carries several price entries **on different units** (one product returning both "$150 per User" and "$1,231 per Multiple"), name the unit with every figure and never collapse them into one number. **Absent-data branch:** where a product carries no list price, say IDC has no list price for that vendor rather than presenting a missing price as zero. An empty deal count or price score is the norm, not a finding.
3. **Stability and consolidation leverage.** Pull the vendor-grain profile for structured financial standing — annual revenue, funding type, founding year, associated companies — rather than scraping stability from prose, and add the strategic-direction read from the narrative on top. Funding type is the most negotiation-relevant field: it shapes how much a vendor needs the deal and how exposed the tech leader is on a long contract. Write an unknown revenue as "not disclosed" — for a multi-year commitment that absence is itself a finding. **Cross-market presence is what makes bundle leverage concrete:** the commercial payload repeatedly advises consolidating spend across a vendor's portfolio, and that advice is only actionable once you can name the adjacent markets the vendor holds and its tier in each. Pull it before offering any consolidation or cross-sell leverage point, and never assert portfolio leverage the profile does not evidence.
4. The tech leader's own stated deal terms are conversational input, never IDC data.
5. **State the limit of the advice.** IDC does not provide legal advice on commercial terms. Say so once in the stage and repeat it in the guide.

**Presentation — the commercial read.** A tight executive brief, roughly one page and never more than two. Open with a one-line bottom-line-up-front on where the leverage sits, then short titled sections — **Discount posture**, **Your leverage**, **List pricing to anchor against**, **Watch-outs** — written as prose, not a bullet dump. Surface the key metrics (discount range, list prices with their dates) as a small highlighted figures block, and pull one sharp analyst line as a quote if the narrative offers one. Keep it forwardable: a procurement lead should be able to send it as is. Cite by source class — the core content is the Class 3 Commercial Dataset, unlinked, with the unlinked Class 1 MarketScape entry only where a tier or narrative line is used. Where the reader is outside procurement, include the general negotiation guidance a non-procurement buyer needs rather than assuming deal fluency.

**Three paths, not equally defined — say which is in play.**

- **Path 1, the self-serve guide.** What this route builds, per `references/sourcing/exports/negotiation-guide.md`. It names the vendors the tech leader asked about, summarises what they asked for, states the leverage assessed, carries the same citations into the file, and states plainly that IDC does not provide legal advice on commercial terms. Once built, the body ends with the vendors covered, a one-line summary of the requests, and the download link.
- **Path 2, a review of a revised RFP or of vendor responses.** No defined artifact. Read the responses against the standing requirements and give the commercial read in chat, and say a formal review artifact is not yet defined.
- **Path 3, a deal review.** An IDC analyst process, not anything generated here: authored by IDC and returned to the tech leader, gated on Tech Leader package entitlement and its own terms. Hand it off — say what it covers, that it is analyst-delivered, and that entitlement applies, without asserting entitlement was checked. Never generate a document that looks like a deal review, and never state a turnaround, because none is defined.

Deep quote or contract analysis beyond list price is out of scope; say so.
