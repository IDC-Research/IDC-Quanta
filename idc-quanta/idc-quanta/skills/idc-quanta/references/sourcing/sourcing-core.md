# Route: sourcing — core

Read on every sourcing request, **before any tool call**, alongside `references/sourcing/rules-sourcing.md`. Carries the pacing, the ledger, the checkpoints and the presentation discipline shared by all six stages. Stage bodies live in `references/sourcing/sourcing-brief.md` (1–2), `references/sourcing/sourcing-selection.md` (3–4) and `references/sourcing/sourcing-artifacts.md` (5–6).

**Purpose:** take a technology leader from an unshaped need to a sourcing decision.

## The workflow is method. It is never output.

Everything these files say about *how* to do the work is instruction to you, not content for the tech leader. Never write into a response: how a figure was computed or which dataset it came from beyond the citation; that a check was run and found nothing ("no adjacent-cut risk here", "every requirement mapped cleanly") — silence is how a clean check is reported; why one method was chosen over another; or reassurance about your own process.

### Plain words, not IDC's rating vocabulary

**Full Support**, **Partial**, **No Support**, *rated elements*, *scorecard*, *axis*, *element*, *sub_element* are internal terms. They never appear in a response.

| Internal | Write |
|---|---|
| Capability coverage, 335/457 rated elements | **Capabilities covered: 335 of the 457 IDC assesses in this market** |
| Full Support on an element | the vendor **fully supports** that capability |
| Partial Support | **partially supports** it |
| No Support | **does not support** it |
| Axis / element / sub_element | the requirement, or the capability |

**Keep the number and its denominator.** "335 of 457" is what stops a 1.00 score reading as "best product overall".

**The numerator counts the capabilities the vendor fully supports.** Partially supported and partner-delivered capabilities are not counted, so a vendor's real reach can exceed its figure. Use that same basis for every vendor in a response, and where a partial matters to a requirement the tech leader stated, say so in that vendor's line rather than letting the count carry it.

### Every Presentation block is a closed list

Where a stage says "four things and nothing else", that is literal: no preamble, no commentary after, no fifth thing you judged useful. **Brevity comes from shortening an element, never dropping one**, and length is never a reason to omit a stage.

The closed list bars your own additions, not a disclosure these files require. Conditional mandated sentences fold into the nearest listed element rather than standing as new sections: tier and grain conflicts go in the per-vendor line for the vendor they concern; the tie-break statement, the must-NOT-have disclosure and the collapse offer go in the completeness line; assumptions from a skipped card go in the confidence line, not the stage 2 table, which stays table-only.

## Six stages, one journey

| # | Stage | Produces |
|---|---|---|
| 1 | Market identification | The named IDC market and a one-sentence definition |
| 2 | My requirements | Requirements sorted functional / technical / company, critical vs non-critical |
| 3 | My shortlist | A ranked, scored vendor list with products, tiers and rationale |
| 4 | Comparison | One row per vendor — strengths, weaknesses, unique capabilities — top 3–5; always with stage 3 |
| 5 | Build the RFP | The RFP plus its vendor response template, when picked at turn 3 |
| 6 | Negotiation preparation | A commercial read when asked; a guide when picked at turn 3 |

**Three statuses, these words only:** **Completed** (ran this engagement, or established earlier and still standing) · **Skipped** (deliberately not run) · **Outstanding** (not reached yet).

The Status cell holds the status word alone. Why a stage was skipped, or what an Outstanding one waits on, goes in Key output so every row has three filled cells. Never invent a fourth status, never leave a stage off the ledger, never mark one Completed on inference.

**The one provisional case:** a stage 1 market call awaiting confirmation is the only stage that may carry a body while Outstanding. Mark it `Outstanding`, Key output `Provisional: <market name> — confirm the cut`, and give it a normal body. Every other stage: no body unless Completed.

## Four turns — 0 to 3. Never all six stages at once.

| Turn | Renders | Checkpoint |
|---|---|---|
| **0 — intake** | The interactive question card alone | The card is the turn |
| **1 — the brief** | Stages **1 and 2** only | "Anything to change, or shall we build the shortlist?" |
| **2 — the selection** | Stages **3 and 4** only | "Any vendors to add, or shall we move to deliverables?" |
| **3 — deliverables** | Header, headline, ledger, then the artifact menu | The tech leader picks |

**Never run ahead of the checkpoint.** On turn 1 you do not score a shortlist and you do not pull vendor detail or commercial data, apart from the single stage 1 naming read. (The market's capability ratings are pulled on **turn 0**, to choose the card's reference criteria — that is turn 0's work and is never repeated.) The market and the requirements are the whole of turn 1. On turn 2 you do not build an RFP, a guide or any export.

**A checkpoint is a real stop.** End the turn and wait. Do not answer your own question, assume a proceed, or append "meanwhile, here's the shortlist".

**Corrections re-render the same turn**, not the next one, with the change applied and the checkpoint asked again — as many rounds as the tech leader wants. Only an explicit proceed advances.

## Ledger — mandatory on every sourcing response

First thing in the body, immediately after the `##` headline, before any stage body. All six stages every time, one line each, Key output a short phrase rather than a second copy of the content. Never dropped for brevity, never moved below the content.

```
**Sourcing progress**

| Stage | Status | Key output |
|---|---|---|
| 1. Market identification | Completed | Accounts Payable Automation Software — midmarket |
| 2. My requirements | Completed | 6 critical, 3 non-critical |
| 3. My shortlist | Outstanding | Next step, once you confirm the brief |
| 4. Comparison | Outstanding | Follows the shortlist |
| 5. Build the RFP | Outstanding | Not yet reached |
| 6. Negotiation preparation | Outstanding | Not yet reached |
```

A response carrying a shortlist shows stage 4 `Completed` with its table in the body; stage 4 `Outstanding` beneath a completed shortlist is a defect.

**One unit everywhere.** The market grades vendors *and* product areas, and the counts differ when a vendor sells more than one product here. Fix the unit before writing the headline and use it in the headline, the Key output cell and the completeness line, naming it each time. Never state a survivor count computed over product areas against the vendor count.

Stage bodies run under `###` headings in exactly this form: `### Stage 3 — My shortlist`. Do not renumber, abbreviate or re-title. Close with **Recommendations** as a bold label, not a heading.

**On a paced turn, Recommendations carries IDC's take and nothing else — not the next step.** The checkpoint that follows is the next step. Only on a mid-journey response with no checkpoint after it does Recommendations also name the next move.

## Body shape by turn

| Turn | Shape |
|---|---|
| 0 | The question card alone. No wrapper, header, ledger or body. |
| 1, 2 | Header → `##` headline → ledger → this turn's stage bodies → **Recommendations** → **Sources** → disclaimer. Then the checkpoint as a question-tool call after the message; with no question tool, the plain-text line goes immediately before Sources. |
| 3 — menu | Header → headline → ledger (1–4 Completed, 5–6 Outstanding) → **Sources** → disclaimer → the menu. No stage bodies, no Recommendations. Sources still required: the ledger names the market and the ranked vendors, so carry the entries those rest on, renumbered from `[1]`. |
| 3 — built artifact | Full wrapper: header → headline → ledger with the built stage now Completed → that stage's short body → **Recommendations** → **Sources** → disclaimer. |

## Checkpoints, verbatim

Close the turn with the question tool where the runtime has one — the call goes after the message.

**Checkpoint 1**, after stages 1 and 2. Header `Next step`, question "Anything to change, or shall we build the shortlist?":
- `Proceed — build the shortlist` — "I'll score the graded field against these requirements."
- `I have changes` — "Correct the market, add or remove requirements, change what's critical."

Plain-text fallback: *"Does this brief look right? Tell me anything to change, or say proceed and I'll build the shortlist."*

**Checkpoint 2**, after stages 3 and 4. Header `Next step`, question "Any vendors to add, or shall we move to deliverables?". This is also where vendors get added, the one thing the intake card deliberately does not ask:
- `Proceed — move to deliverables` — "I'll show you what I can produce from this."
- `I have changes` — "Add a vendor to the assessment, drop one, or adjust the requirements and re-score."

Plain-text fallback: *"Any vendors you'd like added to the assessment, or anything to adjust? Otherwise say proceed and I'll show you the deliverables available."*

**A vendor added here is scored, not inserted.** Run it through the same scoring and place it on its merits, then say plainly where it landed and why — including when it ranks below the presented set or fails a requirement the tech leader stated. Naming a vendor is not a promotion. A vendor they ask to *drop* is excluded in the scoring step and disclosed as their direction (P3/P4).

**Checkpoint 3 — the artifact menu.** In `references/sourcing/sourcing-artifacts.md`. It is mandatory: every full engagement reaches it, so the RFP and negotiation preparation are always put in front of the tech leader.

## Entry points and gating

A tech leader rarely starts at stage 1. Run only the stages the request needs, mark the rest honestly, and carry completed stages forward — a market confirmed in turn one stays Completed in turn six and is never re-asked.

| The request | Run | The rest |
|---|---|---|
| **Any first request for a selection** — "who should we consider", "build a shortlist", "we're replacing X", "where do we start" | **None — resolve, then ask the intake questions** | No ledger, no stage bodies; the card is the whole response |
| The intake answers come back | **1 and 2**, then checkpoint 1 | 3–6 Outstanding |
| Proceed at checkpoint 1 | **3 and 4**, then checkpoint 2 | 5 and 6 Outstanding |
| Proceed at checkpoint 2 | The artifact menu, then whatever they pick | 1–4 stand |
| "Compare A, B and C" | 1 (resolve from the named vendors, confirm by name), 4 — then **checkpoint 2** | 2 and 3 Skipped — they supplied the set, so no selection ran |
| "Shortlist X and compare the top three" | Still paced: intake, then 1–2, then 3–4 | Naming the end state does not skip checkpoints |
| "What's our leverage with A?" / discount posture, list pricing | 1, 6 — no checkpoint; answer, then stop. Where the named product and the user's size map to one graded market, state the market call in the stage 1 body and proceed. Where they don't, ask which market before stage 6 (I1) | 2, 3, 4 Skipped. Close by naming the shortlist and the RFP as available, in one sentence |
| "Build the RFP" (after a shortlist) | 5, on the standing 1–3 | 6 Outstanding. Close by offering negotiation prep |
| "Help me negotiate with the winner" | 6 | 1–5 stand. Close by naming what else the menu offers |
| Requirement change before the shortlist exists | Re-render 1 and 2, then checkpoint 1 again | 3–6 Outstanding |
| Requirement change after the shortlist exists | Re-render 3 and 4, then checkpoint 2 again | Say plainly that 5 and 6, if produced, are now behind — never silently reissue |

**Stage 4 has no "not yet" state when a shortlist exists.** The only rows above where it is not Completed are those where no selection ran.

**Downstream invalidation.** When an upstream change invalidates a stage that already ran, mark that downstream stage Outstanding again and say which change did it. Never quietly overwrite a document the tech leader may already have sent to vendors.

**An engagement entering mid-journey still gets the offer.** Where a request skips to one stage, turn 3's menu never runs, so close by naming the other deliverables still available, in one business-formal sentence. The only case where 5 and 6 go unoffered is a request scoped to exclude them.

## Failure and honesty

- **Shortlist cannot be generated** from confirmed requirements: "We weren't able to generate your shortlist. Your conversation has been saved." Offer a retry, then IDC support. Never substitute training-data vendors for a failed call.
- **A thin market is not a shortlist** (I2a), and **a coverage gap must be proven** (Rule 8a in `references/sourcing/rules-sourcing.md`). A market Tech Leader does not cover has no fallback (Routing).
