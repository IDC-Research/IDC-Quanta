# Route: sourcing — core

Read on every sourcing request, alongside `references/sourcing/rules-sourcing.md`. This is the whole sourcing workflow. Export file specs are in `references/sourcing/exports/`.

**Purpose:** help a technology leader get from a need to a purchase decision, through conversation.

## How the route works

The engagement moves through six phases as a conversation. Each phase ends with a one-line offer of the next one, and the user's plain reply ("yes", "add X", "drop Y") moves it on or reworks the current phase. There is no intake form and no progress table.

| # | Phase | Produces | Ends with |
|---|---|---|---|
| 1 | Market identification | The IDC market (or markets) and a one-sentence definition | Straight into phase 2 when one market fits; the market question when it doesn't |
| 2 | Requirements | What the user needs, mapped to IDC's requirement catalog | "Anything to add or change, or shall I build the shortlist?" |
| 3 | Shortlist | Up to 8 scored vendors per market, with tiers and rationale | "Does this shortlist look right? Want me to build a side-by-side comparison of the top vendors?" |
| 4 | Comparison | Strengths, weaknesses and unique capabilities for the top 3–5 | "I can build an RFP or a negotiation guide from this." |
| 5 | RFP | The RFP plus its vendor response template | "Want me to prepare you for the negotiation once responses are back?" |
| 6 | Negotiation preparation | A commercial read in chat, or a guide file | "Anything you want adjusted before you take this into the room?" |

**Where the conversation starts:**

| The request | Run |
|---|---|
| A new need ("we need X", "who should we look at") | Phase 1, then phase 2 in the same reply (or the market question first, where needed). Where the user asked who to consider, also name the vendors IDC grades in the market (names only; tiers come with the shortlist) |
| A shortlist asked for outright ("build a shortlist", "rank the vendors") | Phases 1 to 3 in one reply (the market question first, where needed), then offer the comparison |
| "Compare A, B and C" or "A or B?" | Phase 1 from the named vendors, then phase 4 for those vendors. Where the user asks which to pick, give a recommendation conditioned on their situation, grounded in the data |
| Pricing, discount or leverage on a named vendor | Phase 1, then the commercial read (phase 6) |
| A quote or contract shared, a deal review asked for, or a question about the user's own negotiation | Phase 1 where a market is needed, then the commercial read (phase 6), within the limits under Phases 5 and 6. Add the Deal Review pointer per `references/deal-review.md`, which sets how often |
| A negotiation question naming a market or category but no vendor ("a major cloud infrastructure vendor") | Phase 1 to confirm the market, then answer from IDC research on that market's commercial and contract norms. The Commercial Dataset is per vendor, so do not run a per-vendor read on an unnamed vendor: offer in the closing line to run one once they name the vendor. Add the Deal Review pointer per `references/deal-review.md`, which sets how often |
| IDC's guidance on negotiating a class of contract, no vendor or market named | Document search for the relevant IDC research, answered on this route with no Phase 1 and no scores or tiers. In the Tech Leader package, where document search is not available, say the underlying research sits outside this package and let the pointer carry the next step. Add the Deal Review pointer per `references/deal-review.md`, which sets how often |
| An RFP or negotiation guide | The prerequisites check under Phases 5 and 6 |

Run one phase at a time unless the request asks for more, and do not run ahead of what the user asked for.

**Where several phases run in one reply, every phase still renders its own artifact.** Phases 1 to 3 in one reply means the market named with its scope and definition, the requirements table, and the shortlist table with its field line — not the shortlist alone. Compression shortens the prose between them; it never drops one of the three. The reply carries one closing line, the one for the last phase run. A correction reworks the current phase and asks its closing line again.

Read the tool descriptions and decide the calls yourself. Use as many as the answer needs and no more.

## Phase 1 — Market identification

1. **Search the Tech Leader market catalog** with market context enrichment on, and consider every plausible candidate. Use market search for this step rather than market category search.
2. **Get the counts cheaply.** The market record gives the product count. The market-filtered vendor listing gives the roster, and its distinct vendor ids give the vendor count. Pull counts only for markets you work in, not for markets you pass over.
3. **Choose by what the user is buying, not by which catalog grades the most of their requirements.** A requirement the closest market does not grade is disclosed as not graded. It is never a reason to switch to a different product category.
4. **Where the need spans more than one market,** say so and work each market separately. Scores, counts and rankings never merge across markets.
5. **Run the sanity check** (below) before presenting the market call.
6. **Name the market with its scope.** Take the catalog name, then the company-size, regional or industry scope from the market record or, where the record states none, from one vendor detail narrative ("the 2024 IDC MarketScape for worldwide modern endpoint security for midsize businesses"). Each product also carries a target company size (for example Enterprise-only, or Enterprise-MidMarket). Where neither the market nor its narratives state a cut, omit it rather than labelling its absence. Never invent an employee band. State one only where IDC's data publishes it (a company-size requirement row, for example). Say which cut you used and, where the user's size may sit at its edge, say so plainly.
7. **One market fits: say so and go straight into phase 2** in the same reply:

   > IDC's closest market in your coverage is **<Market name with scope>** — <one-sentence definition> [n]. If you meant something else, let me know.

   That is a shape, not a fixed string: keep the three elements — the market named with its scope, its one-sentence definition cited, and the invitation to correct it — and word the rest naturally. (The closing lines and the Deal Review pointer are the fixed strings; this is not one of them.)

   Then list any market you passed over, one line each with the reason, and continue with the requirements.

8. **No single market fits: ask the market question.** This applies when what the user is buying spans two or more markets, or maps to no market directly. A nice-to-have that IDC grades in its own market (MDR alongside endpoint security, for example) does not trigger it: note that market in the requirements instead. Search on broader and adjacent terms, use capability-prose search to find markets whose vendors describe the capability, and scan the full market catalog listing (one call) before concluding no market matches. Read each candidate's definition and keep only markets whose definition fits the need, since search ranks by wording, not fit. Run the sanity check, then ask one question and stop. Use the question tool where the runtime has one:

   ```
   questions: [
     { header: "Market", multiSelect: false,
       question: "Your need spans more than one IDC market. Which should I assess?",
       options: [
         { label: "<Market A> (Recommended)",
           description: "<one-sentence definition>. <N> vendors graded." },
         { label: "<Market B>",
           description: "<one-sentence definition>. <N> vendors graded." },
         { label: "Assess each market separately",
           description: "I'll capture your requirements once, then build a separate shortlist for <Market A> and <Market B>." } ] } ]
   ```

   Two or three markets, the best fit first, then the separate-assessment option last, naming the markets it would assess. Where two candidates cover the same part of the need, offer both as options and let the separate-assessment option name one market per part. Where the need maps to no market directly, word the question "IDC assesses this need within related markets. Which is closest to what you're buying?". The question card is the whole turn: no header, body or disclaimer. With no question tool, ask the same thing in plain text: the markets as a short list with definitions, then "Or I can assess each separately."

   After the answer, run phase 2 for the chosen market, or for every market where they chose separate assessments.

Where the user named vendors that IDC grades together only in an adjacent market, say which product each is graded on there, compare on that basis using tiers and narratives rather than fit scores, and, in the Full package, add IDC research on the category itself. Skip the "score the whole market" next-step line in that case. This case needs no market question.

9. **Phase 1 is not only the gateway to phase 2.** Wherever the route reaches phase 1 — including a pricing, discount or leverage question that runs phase 1 and then the commercial read, with no requirements and no shortlist in between — the market is still named to the user per step 7, with its definition and citation. The Class 3 market name in the Sources entry is the name set here (Rule 3a), so a commercial read that never named the market leaves its own citation unanchored. Drop only the hand-off into requirements.

## Sanity check

Before you present a market call or a shortlist, check that the result fits the need.

- **Candidate vendors the user named.** Search each one and see which markets grade it. If a named candidate is graded in a different market from the one you chose, reconsider the market or treat the need as spanning both. A system the user is keeping (their ERP, for example) is an integration requirement, not a candidate.
- **Category leaders.** The vendors a buyer in this category would expect to see should be graded in the market you chose. If they are graded elsewhere in the Tech Leader catalog, that is a sign of a wrong or partial market call.
- **Full package:** use IDC research and share data to see who leads the category and to test the market call. The MarketScape citation lookup (`rules-sourcing.md`, Rule 3a) helps here too. This never adds a vendor, score or tier to the shortlist.
- **A newer edition.** Where IDC research shows a newer IDC MarketScape for the same market and the same company-size cut than the Tech Leader data reflects, keep the Tech Leader tiers for the shortlist and add one cited sentence naming the newer edition, so the user can read it.
- **Tech Leader package:** run the check within the Tech Leader catalog only. That is the full coverage of this package.

When the check changed the market call, say what it changed in one sentence ("Slack is graded in Team Collaboration, so I've used that market"). When it confirmed the call, say nothing about it.

## IDC context (Full package)

In the Full package, every IDC tool is available. Prioritize the Tech Leader tools: they carry each phase of the sourcing workflow. Add the Quanta tools wherever they make the answer more complete:

- **Market identification and requirements:** market size, growth and share leaders for the category, and IDC research on what buyers in this market prioritize.
- **Shortlist and comparison:** each vendor's share position and momentum, recent moves, and analyst views from IDC research, beside the Tech Leader scores.
- **Negotiation:** IDC research on pricing trends and the vendor's position, alongside the Commercial Dataset.
- **Questions the Tech Leader data doesn't cover** (peer experience, growth, roadmap, sizing): answer them from IDC research and data within the engagement.

Two rules keep the shortlist trustworthy. Shortlist rank, fit scores and MarketScape tiers come only from the Tech Leader scoring engine and data. Quanta context sits in its own lines or a short IDC context block, cited in the linked Rule 3 form, so the reader can tell scores from context. Pull what the question needs, no more. For context, one IDC document search (a Market Share or Market Glance document) usually gives the figures, the analyst commentary and a live link in one call: prefer it to a multi-step Tracker query unless the user asks for the figures themselves. Where a document and a Tracker give different figures for the same measure, use the Tracker figure and keep it consistent across the conversation. Share or growth claims inside the Commercial Dataset text are not current share data: in the Full package, use IDC share data instead; in the Tech Leader package, leave them out.

In the Tech Leader package, none of this applies: answer from Tech Leader data only.

## Phase 2 — Requirements

- **Take requirements from what the user wrote,** in any form. Do not ask them to sort, rank or label anything. Nothing needs to be marked critical or nice-to-have.
- **Map each one to the market's requirement catalog** so it can be scored. Where a related catalog criterion fits, say it is scored through that criterion. A requirement outside the catalog stays on the list, marked "not graded by IDC", and carries through to the RFP as a question for vendors.
- **Where the user gave none, or only one or two,** add catalog criteria where the vendors actually differ, so the scores separate the field. Say briefly which you added. Never stop to ask for requirements.
- **Mixed markets.** Where a market grades several product types (chat platforms alongside work-management and whiteboard tools, for example) and the user named the type they are buying, add the catalog's product-focus criterion for that type at raised weight, whatever else the user gave. Say you did.
- **Show the requirements compactly:** a short table of what you captured and how IDC grades each (graded, scored through a related criterion, not graded). Group them however reads best.
- **Separate assessments:** capture the requirements once and map them to each market's catalog. A table with one grading column per market shows where each is graded.
- **Must-not-haves:** look for a catalog row already phrased as an absence ("does not require an additional agent") and score it. Where none exists, check vendors against the ratings or narrative after scoring and drop clear violators, saying so. Keep a vendor whose evidence is inconclusive, flagged.

**Close the phase** with "Anything to add or change, or shall I build the shortlist?". A change reworks the table. A yes moves to phase 3.

## Phase 3 — Shortlist

1. **Score with the scoring engine** (`rules-sourcing.md`, Scoring engine). Leave priorities at the engine's default unless the user signals importance. Raise what the user emphasizes to the engine's HIGH priority ("raised weight" everywhere in this file means HIGH). Use the engine's hard-filter priority only where the user says a vendor must have the capability or is out ("must", "non-negotiable", "won't consider without"). A plain "we need" is a requirement at normal or raised weight, not a hard filter. Criteria you added are never hard filters.
2. **Qualifiers and logic.** Where a requirement has qualifiers, select the ones that match what the user means, including close variants, not only their literal words. Use "or" unless the user needs every option. Where two readings give materially different results, use the closer one and say which reading you used.
3. **Thin results.** If fewer than five vendors fully meet the user-stated must-haves, show what survived, say which requirement narrowed the field, and offer to relax it. At two or fewer, also show the result with it relaxed and let the user choose. To find which requirement narrowed the field, re-score without each must-have in turn (one call each) and see which brings vendors back. When the user asks you to choose what to relax, take the must-have that removes the most vendors, move it from hard filter to raised weight, keep the rest, and say what you changed.
4. **Partial support on a must-have.** The engine keeps a vendor that partially supports a hard-filter requirement, at a lower score. Count only full supporters when saying how many vendors meet a must-have, and say "partially supports <requirement>" in that vendor's line.
5. **Evidence.** For every vendor shown, pull the market-scoped vendor detail: tier (the narrative tier is authoritative, P0-1), strengths and challenges. Take capabilities covered from the market's vendor ratings. Pull the vendor profile (revenue, funding type, cross-market presence) for the top 3–5 only. Write an empty financial field as not disclosed.
6. **Present up to 8 vendors by default** (more if the user asks) in a table: rank, vendor, product, fit score (as the engine returns it, two decimals), IDC MarketScape tier, capabilities covered. Put the edition year and company-size cut in the table title. Order tied scores by capabilities covered and number the ranks in the order shown. This tie order is the only reordering of the engine's ranking. One or two lines per vendor on why it ranks there and its main watch-out. Where a vendor's product is a different type from what the user is buying (a whiteboard tool in a chat-and-meetings search, for example), say so in its line. Where the top rank is a tie, say the leaders are tied on fit score.
7. **Account for the field** in one or two sentences: how many vendors the market grades and who is not shown, with the reason where known. Where the cut falls inside a tie, say so plainly ("tied on fit score; the vendors shown cover more capabilities").
8. **Where the need spans markets,** give one shortlist per market. Where the markets warrant different confidence, the confidence line gives the lower one and names the market it applies to.

**Close the phase** with "Does this shortlist look right? Want me to build a side-by-side comparison of the top vendors?". Do not build the comparison in the same reply unless the user asked for it.

A vendor the user asks to add is scored and placed on its merits. If it ranks below the cut, add it as an extra row beneath the table with its rank ("Mattermost — rank 9 of 15"). Do the same for any IDC MarketScape Leader in this market that ranks below the cut, with its fit score. Find the market's Leaders in the MarketScape document (Full package) or in the vendor details already pulled. Name the requirement it scored lower on only where data already pulled shows it; do not pull full ratings just for this. A Leader removed by a must-have is named in the field line with the must-have it does not meet. A category leader is never silently missing. A vendor they rule out goes to the engine's discard list, stated as their direction.

**Capabilities covered** is the number of capabilities IDC rates the vendor as fully supporting, out of the sum of every rating bucket the market's vendor ratings summary reports for that product (not the separate element count). Partial and partner-delivered support are not counted. Use the same basis for every vendor in a response, and write it as "137 of 209". Where the figure needs explaining to the user, say "how many of the capabilities IDC rates in this market the product fully supports" — never "graded elements", "rated elements" or any other internal label (Plain words, below). It is a breadth measure across everything IDC rates in the market, not a measure of fit against the user's requirements, which is what the fit score is; say so in one line wherever a vendor with broader coverage ranks below one with narrower coverage.

## Phase 4 — Comparison

Produce it when the user accepts the shortlist or asks for a comparison: the top 3–5 by default, or the vendors the user names. Reuse the vendor detail already pulled for the shortlist. One row per vendor: **Strengths**, **Weaknesses**, **Unique capabilities**, a few phrases per cell. Unique capabilities come from the ratings where they settle it, otherwise from the narratives, relative to this group only. Beneath it, one line per vendor with tier, edition year, IDC capability score (0–100, MarketScape's capability rating), capabilities covered (breadth) and company-size cut.

**Close the phase** with "I can build an RFP or a negotiation guide from this."

Compare products rather than vendors when a vendor sells more than one product in the market. A criteria matrix or a list-price view is produced on request. Peer experience, growth momentum and roadmap trajectory sit outside Tech Leader ratings. In the Full package, answer them from IDC research and data (IDC context, above). In the Tech Leader package, say so rather than inferring.

## Phases 5 and 6 — RFP and negotiation preparation

**Before building either file, read its export spec and check what it needs.** If something is missing, ask once, in one short message that names only what is missing, and offer to create what the engagement lacks. This question needs no tool call. For example:

> To build a proper RFP I still need <what is missing, e.g. your requirements and the vendors to invite>, plus your due date and submission contact. Want me to <create the missing piece, e.g. build the shortlist> first?

| Artifact | Needs from the engagement | Needs from the user |
|---|---|---|
| RFP + response template | Market, requirements, invited vendors | Due date, submission contact, questions cut-off, evaluation weighting; their own template if they have one; short or full form (default short) |
| Negotiation guide | Market, the vendor(s) taken forward | Budget ceiling, contract renewal or end date, alternatives seriously in play, who will be in the room and whether they are procurement professionals; PowerPoint or PDF |

Fold the spec's own pre-build checks (catalog requirements never discussed, requirements scored through a related criterion) into the same message. Where the category is not graded as its own Tech Leader market, the RFP can still be built on the user's requirements: say the vendor set comes from the closest graded market or from the user, and offer to draft requirements from the catalog only where that market grades the product being bought. Ask the user only for what only they know. Never ask them for a vendor's fiscal year-end, discount posture or funding: pull those from the tools.

**Commercial read in chat.** Any pricing, discount or leverage question gets an answer in chat without a file. Per vendor: discount posture and leverage points (IDC analyst guidance from the Commercial Dataset), list pricing with each date inline and its unit named, flagged stale when over 16 months old, and stability from the vendor profile. Where IDC rates a discount range rather than a figure, give IDC's rating and say IDC's guidance is expressed as a rating, not a fixed percentage. Never supply a number IDC did not publish. A list price that looks implausible for its unit is shown as listed and marked "to confirm with the vendor". Where commercial data or a list price isn't included for a vendor, say so, without implying there is no leverage. Where commercial data exists only for the vendor's product in an adjacent market, it may be used, named as that product's data. Competing vendors in the same market may be used as leverage where IDC grades them. State once that IDC does not provide legal advice on commercial terms. A review of vendor responses gets a commercial read in chat, with no file.

**Where the commercial read stops short.** The read delivers IDC's published commercial data. It does not deliver a verdict on a deal the user actually has, because that is the Sourcing Advisory analyst's work. So the published figures stay — list price with its date and unit, discount posture, any published range — and three things never appear: a figure aimed at their own deal (a target price, a discount to hold out for, what their renewal should come to, or arithmetic on a figure they supplied); a judgment on whether their price, discount, uplift or terms are good, fair, high, low or unusual; and any commentary on a document they shared beyond using it to identify what to research. Where the user has shared a quote or contract, read it only to find the topics, answer those from IDC research, and quote none of it back.

Such an answer carries the Deal Review pointer, which is where the deal-specific read actually happens. `references/deal-review.md`, owns when it appears and how often — it is not on every commercial read, only where that section says — and this file does not set its own frequency.

Collecting the inputs an export needs is unaffected: a budget ceiling, a renewal date or an incumbent is a prerequisite for Phase 5 or 6, not a figure for you to judge. Ask the user for it and use what they state in conversation. Do not lift it out of a quote or contract they shared, even where it appears there (`exports/negotiation-guide.md`).

Build files per `references/sourcing/exports/common.md` and the matching spec.

## Carrying context forward

Keep the market, the requirements and what has been built in mind across turns, and build on them without re-asking. IDC data already pulled in this conversation can answer a follow-up, such as a scoring read-back or a commercial question on a vendor already pulled; there is no need to call the tools again for it. When a change makes something already built out of date (an RFP built on an old shortlist), say so where it matters and offer to rebuild. Never rebuild silently.

**Progress line.** From the second sourcing reply in an engagement, put one line directly under the headline showing where the engagement stands:

```
Market: Team Collaboration · Requirements: 11 captured · Shortlist: built · Next: comparison
```

- **Market:** the market name, or "2 markets" for a separate assessment.
- **Requirements:** the number captured.
- **Shortlist, Comparison, RFP, Negotiation guide:** include each only once it has been built or asked for, marked "built" or "out of date".
- **Next:** the phase the closing line offers.

Plain text, one line, no table. Leave it out of the first reply, the market question card, the prerequisites question, the fixed package replies and the scoring-methodology brief.

## Body shape

Header → `##` headline → the progress line (from the second reply) → the answer → the closing line → the Deal Review pointer where it applies (`references/deal-review.md`) → **Sources** → disclaimer. Where a reply has no closing line, the pointer sits at the end of the body instead, still before **Sources**. This shape governs sourcing responses wherever another reference file describes a different one, with one named exception: the scoring-methodology brief follows the shape in `references/sourcing/scoring-methodology.md`, which carries no progress line and no closing line because it explains a result rather than advancing the engagement. There is no progress table or stage ledger: the one-line progress line replaces them.

**Closing lines.** Close the answer with the line for the phase just completed:

- Requirements shown: "Anything to add or change, or shall I build the shortlist?"
- Shortlist shown: "Does this shortlist look right? Want me to build a side-by-side comparison of the top vendors?"
- Comparison shown: "I can build an RFP or a negotiation guide from this."
- A comparison of named vendors shown: "Want me to score the whole market to see who else fits your needs?" plus the RFP and negotiation guide line
- Commercial read shown: "Want me to turn this into a negotiation guide you can take into the room?"
- Contract or negotiation research shown with no vendor named: "Name the vendor and I can pull IDC's commercial read on them."
- RFP delivered: "Want me to prepare you for the negotiation once responses are back?"
- Negotiation guide delivered: "Anything you want adjusted before you take this into the room?"

Use one closing line per reply, the one for the phase just completed. The scoring-methodology brief is the one sourcing reply with no closing line. A market intelligence follow-up inside an engagement closes with the line of the phase the engagement is in.

**Write for the customer.** Every sentence must help the user decide. Tell them what changes the answer: the market chosen and why others were passed over, requirements IDC does not grade, vendors not shown and why. Citation numbers go on IDC content only, never on your own choices. Leave out how the answer was produced: tool names, ids, call sequences, data reconciliations, field-versus-narrative conflicts, scoring mechanics beyond one plain phrase, and checks that found nothing.

**Plain words.** Write "fully supports", "partially supports", "does not support" and "capabilities covered: 137 of 209". Do not write Full Support, rated elements, axis or sub_element. Keep the denominator beside every count. This governs prose, in chat and in files. It does not govern a column header or an answer option in the vendor response template, whose labels are set by `references/sourcing/exports/rfp.md` so vendors can complete the sheet without restructuring it.

## Failure

- **A shortlist cannot be generated.** Say why in plain terms and ask for what would help, then try again. Never substitute vendors from general knowledge.
  - *The requirements leave no vendor, or too few* (Phase 3, Thin results). Name the requirement or combination that narrowed the field and ask whether to relax it, lower its weight or swap it for a related criterion.
  - *A requirement could not be matched to IDC's criteria for this market.* Name it, show the closest criteria IDC grades, and ask which reflects what they need.
  - *The market or company size is unclear.* Ask which market or size cut fits, offering the candidates.
  - *The scoring service did not respond.* Say so, retry once, and if it still does not respond, offer to try again shortly or contact IDC support at idc_support@idc.com.
- **A thin market** (under roughly 8 graded vendors) is the market, not a selection: say so. A coverage gap must be proven (Rule 8a).
