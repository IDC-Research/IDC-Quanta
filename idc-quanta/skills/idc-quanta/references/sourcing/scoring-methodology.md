Read this when the tech leader asks how the scoring worked. It defines the scoring-methodology brief — a
full audit trail of the engagement, produced on request and never unprompted.

# Scoring methodology brief

## When to produce it

Produce it when the tech leader asks how the scoring, ranking, selection or exclusions worked. The stage 3
note invites the exact phrase — `Details on Scoring Methodology` — but **any free-form version of the
question triggers this file**: "how did you score these", "why is X ranked above Y", "how was this
calculated", "what was the methodology", "show me your working", "why did Z get excluded", "on what basis".
Do not make them use the magic phrase.

**Never produce it unprompted.** It is a long section and it is not part of a normal sourcing response, so
it goes out only when asked. Nothing about it changes the ledger: it is an explanation of the engagement,
not a seventh stage. Keep the stages as they stand and do not mark anything Completed because the brief
was produced.

**It is a read-back of the engagement, not a fresh analysis.** Every figure in it comes from what already
ran — the same market, the same requirement set, the same scores and the same exclusions the tech leader
has already seen. Do not re-score, do not re-resolve the market, and do not produce different numbers than
the shortlist showed; if the two disagree, the shortlist is what stands and the discrepancy is the finding.
Where a section has nothing to report because that stage has not run, say so in one line rather than
omitting the section.

## Format

A `##` headline, then the six sections below under `###` headings, in this order, then **Sources**, then
the disclaimer. **No Recommendations footer** — the brief explains a result rather than recommending one,
and the engagement's Recommendations stands as last rendered. The sourcing header applies, and so does the ledger — it opens the body as it does on
every response the route produces, with the stages exactly as they stand (the brief changes none of them). Keep it factual and tabular where the content is a list; this is an audit trail, not an essay,
so resist narrative padding. Citations follow Rule 3 and Rule 3a exactly as they do everywhere else: the
market definition to the Vendor RFI entry (Class 3, unlinked), tiers and narrative to the MarketScape (Class 1, unlinked), the engine scores, coverage
denominators and requirement rows to the Vendor RFI entry (Class 3, unlinked), and pricing or discount
posture to the Commercial Dataset entry (Class 3, unlinked).

## The six sections

### 1. The market chosen, and the markets passed over

The market as confirmed, named as stage 1 named it from the market record with the segment scope intact,
its one-sentence definition cited, and its edition year and company-size cut, since the whole ranking
rests on it.

Then every candidate the search surfaced and did not win, up to five, one line each on why, in the same
order stage 1 carried them, labelled by kind: declined by the tech leader on the intake card, or ruled out
by you.

### 2. The requirements, with their priorities

Every requirement in the engagement, in a table: the requirement as the tech leader stated it, its type
(functional / technical / company), its priority as they gave it (critical / non-critical, and the engine
priority it mapped to), its origin (typed on the intake card, stated in conversation, extracted from an
upload, or your own inference, labelled as such), and whether it was scored.

Where a requirement mapped to a catalog row, its type came from that row's own classification rather than from
inference — note that once, since it is the difference between IDC's classification and a judgement call.

**Requirements with no IDC catalog match are listed here explicitly, not quietly dropped.** Mark each one
"not in IDC's requirement catalog — not scored" and say in one line what that means: it shaped the RFP and
the read, but it could not shape the ranking. A tech leader auditing a shortlist needs to know which of
their criteria the engine never saw. Where the intake card was skipped and the scoring ran on the market's
most heavily weighted catalog criteria, say so and list those criteria as assumed rather than stated.

### 3. The shortlist, with scores

Every vendor presented, in rank order: rank, vendor, product, engine score, MarketScape tier, capabilities-covered figure. Then the mechanics, briefly and plainly:

- The score is a weighted match against the stated requirements, tiered by importance, computed by IDC's
  deterministic scoring engine — the same requirements against unchanged data always produce the same
  ranking.
- Scores are **requirement-relative**: they measure fit against this tech leader's criteria, not overall
  product quality, which is why the capabilities-covered figure sits beside each one.
- Ties: the engine orders equal scores alphabetically, which carries no meaning, so tied blocks were
  re-ordered by capabilities covered, descending, before any cut. Name the tied blocks and where the cut fell.
- A **partial** score means partial capability; an **absence** from the returned set means the vendor
  wholly failed a selected requirement. These are different findings and are reported differently.
- Any override the tech leader made — a vendor promoted or dropped against its computed score — with their
  stated reason, and the computed rank it replaced.

### 4. The vendors excluded, and why

Every graded vendor not presented, with the requirement that removed it. Keep the two kinds of exclusion
separate, because they rest on different evidence:

- **Engine-filtered** — the vendor wholly failed a requirement passed to the scoring engine. Name the
  requirement. Where the attribution is uncertain, say so, and note that re-running the scoring with the
  suspect requirement alone settles it in one call.
- **Applied after scoring** — a must-NOT-have the catalog does not carry, enforced by you against the
  rated elements and the vendor narrative. Name the exclusion, name the vendors, and say plainly that this
  cut rests on IDC's rated elements and narrative rather than on a deterministic filter.
- **Excluded at the tech leader's direction** — a vendor they ruled out. Attributed to them, never
  presented as IDC's judgement.

State the graded field size (vendors and product areas, using the same unit as the shortlist) and account
for every vendor. **Never write that vendors were dropped, missing or lost to a data defect** — their own
criteria excluded them, and saying otherwise tells a tech leader a credible option does not exist.

### 5. The inputs that shaped the RFP

Only where an RFP has been produced. Otherwise one line: no RFP has been generated in this engagement.

Which shape was built (lightweight or full formal) and whether it used the tech leader's template or IDC's
default structure; the requirements it carried, including the unscored ones; the evaluation weighting; the
submission instructions given (deadline, contact, questions cut-off); the invited vendor set and its order;
every assumption the document states and every placeholder it enumerates; and its version-and-basis block.
Where the RFP has been reissued or an addendum added, say which version this describes.

### 6. The inputs that shaped the negotiation guidance

Only where a commercial read or negotiation guide has been produced. Otherwise one line: no negotiation
guidance has been generated in this engagement.

Which vendors it covered and what the tech leader asked for; the discount posture and ranges cited, and
that they are IDC analyst-authored guidance rather than hard figures; every list price with its own
date and any price flagged stale; the viability and cross-market presence evidence behind any
consolidation or bundle leverage point; where no IDC commercial data existed for a vendor and leverage
could therefore not be assessed. Repeat that IDC does not
provide legal advice on commercial terms.

## What not to do

- **Do not invent precision.** If a weighting, a tie-break or an exclusion attribution is not recoverable
  from what actually ran, say it is not recoverable rather than reconstructing it plausibly.
- **Do not surface internal mechanics.** Canonical market ids, product-area ids, requirement ids and tool
  names stay out (`references/sourcing/rules-sourcing.md`, Voice and presentation). The tech leader sees market, vendor and
  requirement *names*, and bracketed citations. The single exception is the requirement text itself, which
  is quoted as the catalog words it.
- **Do not re-litigate the ranking.** The brief explains how the result was reached; it does not argue the
  result was right. Where a limitation is genuinely material — assumed requirements, a stale price, an exclusion resting on narrative rather than a filter — state it plainly and let the
  tech leader judge.
