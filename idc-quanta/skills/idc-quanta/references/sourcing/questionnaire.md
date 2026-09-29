# Sourcing intake — the interactive question card

Read on every sourcing request. This is the turn-0 card that captures the market and the requirements before anything is generated.

**It is an interactive question card, not a written form.** Use the session's user-question tool (`AskUserQuestion` where available). Never write out a markdown form and ask the tech leader to fill it in.

**The sequence is fixed.** Make the resolve calls (market search, taxonomy depth, requirement catalog, and the market's per-element vendor ratings) → call the question tool → and only after the answers come back, generate turn 1.

**Nothing renders before the card.** No prose, no ledger, no stage bodies, no partial shortlist, and no narration of the resolve step. The card is the turn.

## When to ask

Ask on any sourcing request involving a **selection** — "who should we look at", "build a shortlist", "we're replacing X", "we need to buy Y", "where do we start". That is the default and it takes no judgement about how much detail the request carried.

**The only four exceptions:**

1. **The tech leader named the vendors to compare** — a stage 4 entry; they supplied the set, so there is no selection to specify. (Naming vendors *and* asking who else to consider is a selection: ask.)
2. **The request is only commercial** — discount posture, pricing, leverage on a named vendor (stage 6).
3. **An engagement is already running with stages 1 and 2 Completed.** Ask once per engagement, never twice.
4. **An upload covers it** — pre-answer what it covers and ask only what is genuinely missing.

**"They already gave detail in prose" is not an exception.** Carry what their message said into the card so they can extend or correct it, and ask the rest. A request naming three requirements has still said nothing about company requirements, exclusions, or what it could live without.

## Resolve first, so the options are real

The market options come from a live call, never from memory: the actual candidates with each one's definition and graded depth in its description.

**Pull the requirement catalog and the per-element ratings on the same turn too**, for two purposes that are not the options: to put a short reference list of IDC's own criteria into question 2's *question text*, and to map the free-text answers onto catalog rows when you score them.

**Pick the reference criteria for discriminating power, not for how common they are.** A criterion every graded vendor satisfies tells the ranking nothing, so read the per-element ratings and choose the rows where the field actually **splits**. Prefer rows already phrased as an absence ("does not require an additional software agent"), since those score as hard filters. One paged ratings call buys this. Where one page cannot show the split (a large market returns thousands of rating rows), single-requirement scoring probes are allowed on this turn to see how many vendors pass each candidate criterion. They are preparation for the card, never output.

## The question set — three questions, one call

Ask exactly these three, in this order, in a single call. Do not add a fourth, do not ask about vendors, comparison, the RFP or negotiation, and do not ask about budget or timeline.

**Question 1 — the market.** Single select. Header `Market`. Question: "Which IDC market covers what you're buying?" Options are the two to four resolved candidates, each labelled by its short market name, with a description carrying the one-sentence definition and the graded depth ("19 vendors graded, midmarket cut, 500–2,500 employees"). Where only one market is plausible, still ask — make the second option the nearest adjacent cut so a wrong resolve is caught here rather than after a shortlist is built. Put the recommended one first, marked "(Recommended)".

**Question 2 — critical requirements.** Header `Critical`. The ask, then a short reference list of IDC's criteria:

> "What are your critical requirements? Type everything the solution must have — in your own words, in any order, as many as you like, and I'll organise them. For reference, the criteria that most separate the vendors IDC grades in this market are: `<criterion 1>`; `<criterion 2>`; `<criterion 3>`; `<criterion 4>`."

**The reference list goes in the question text, never in the options.** Four to six criteria in plain language, drawn from the rows where the ratings show the field splitting, one clause each. Attribute them as IDC's criteria for the market, not as a recommendation: say "the criteria that most separate the vendors here", never "the criteria you should require". They are a prompt, not an answer set — the tech leader is free to ignore every one. Six is the ceiling.

Options: exactly these two, nothing else.

- `Skip — no hard requirements to state` — "I'll score the field on IDC's most heavily weighted criteria for this market and flag every assumption."
- `Not sure — suggest criteria for this market` — "I'll propose the criteria that most separate the vendors here, and you can react to those."

**Question 3 — non-critical requirements.** Header `Nice to have`. Question: "And anything you'd like but could live without? Type those here." Options: exactly these two.

- `Skip — nothing non-critical` — "I'll score on your critical requirements alone."
- `Not sure — suggest some` — "I'll propose a few and you can react."

### Questions 2 and 3 are free-text. Never offer categories.

**Do not put "Functional", "Technical" or "Company" — or any category, axis or requirement type — in the options of question 2 or 3.** Do not offer catalog rows, example requirements, or any list the tech leader could mistake for the answer set. Those two questions have exactly the two options above, and the options exist only as a way out: a skip and an ask-for-help.

The answer is what they **type**. The question tool renders its own free-text choice alongside the options, and that is the primary path for these two. **If a runtime's question tool accepts selections only, it cannot carry these two questions:** ask question 1 through the tool and take the requirements in writing using the free-text part of the fallback form below.

**Sorting those words into functional, technical and company is your job, done silently when you build the stage 2 table.** The tech leader never sees, chooses or is asked about the three categories — not in the card, not in a follow-up, not in a confirmation.

**Skip is a real answer.** Skipping critical means score on the market's most heavily weighted catalog criteria and say so. Skipping both means the same with the whole requirement set marked assumed. Never chase a skip.

### Worked payload

```
questions: [
  { header: "Market", multiSelect: false,
    question: "Which IDC market covers what you're buying?",
    options: [
      { label: "AP Automation — midmarket (Recommended)",
        description: "Software that automates the invoice-to-pay cycle on top of your finance system of record. 14 vendors graded across 16 product areas, 500–2,500 employees." },
      { label: "AP Automation — enterprise",
        description: "The same technology graded for 2,500+ employees. 11 vendors graded." } ] },

  { header: "Critical", multiSelect: false,
    question: "What are your critical requirements? Type everything the solution must have — in your own words, in any order, as many as you like, and I'll organise them. For reference, the criteria that most separate the vendors IDC grades in this market are: line-level three-way matching with tolerance rules; a vendor-maintained certified ERP connector; payment execution over your own banking rails rather than the vendor's network; and supplier onboarding and self-service.",
    options: [
      { label: "Skip — no hard requirements to state",
        description: "I'll score the field on IDC's most heavily weighted criteria for this market and flag every assumption." },
      { label: "Not sure — suggest criteria for this market",
        description: "I'll propose the criteria that most separate the 14 vendors graded here, and you can react to those." } ] },

  { header: "Nice to have", multiSelect: false,
    question: "And anything you'd like but could live without? Type those here.",
    options: [
      { label: "Skip — nothing non-critical",
        description: "I'll score on your critical requirements alone." },
      { label: "Not sure — suggest some",
        description: "I'll propose a few and you can react." } ] } ]
```

## After the answers come back

Generate turn 1 in the same turn. Stages 1 and 2 are `Completed` — the answers are the content.

- **Question 1** confirms stage 1. A non-recommended pick re-resolves the market before anything else.
- **Questions 2 and 3 arrive as free text, and sorting them is your job.** Put each requirement in the right row of the stage 2 table — **functional** (what the solution must do), **technical** (integrations, deployment, security, certifications) or **company** (the vendor itself: size, viability, geography, support model) — in the critical or non-critical column according to which question it came from. **Where a requirement maps to a catalog row, take the classification from that row** rather than inferring it; only an unmapped one needs your judgement. Where one requirement spans two rows, put it in the row that decides whether a vendor can do it at all. Never hand the sorting back to them, and never leave a requirement out of the table because it was hard to classify.
- **Then map each one to the requirement catalog for scoring.** A requirement with a catalog match goes to the engine at CRITICAL (from question 2) or MEDIUM/LOW (from question 3). A requirement with no match stays in the table marked "not in IDC's requirement catalog — not scored" and carries through to the RFP unchanged. A stated must-NOT-have follows the stage 2 exclusion handling.
- **Skipped:** proceed on the market's most heavily weighted catalog criteria, mark the requirements assumed rather than stated, and carry that into the confidence line.
- **Vendors the tech leader mentions** — an incumbent, candidates they like, one they have ruled out — are never asked for on the card. When they come up in conversation: mark candidates and the incumbent in the shortlist table, exclude a ruled-out vendor deterministically in the scoring step and disclose it as their direction (P3/P4), and run the alternatives-beyond-incumbents mode where they ask what else is out there.

**Never re-ask.** Once the card has gone out, further requirements arrive as conversation and update stage 2 in place. Do not re-render the card, and do not follow up on a skip.

## If the question tool is unavailable

Only where the runtime has no interactive question capability (a scheduled or headless run). Say in one line that the answers can come back in any shape.

```
**Before I build your shortlist, three quick things.**

**1. The market.** I've resolved this to **<Market name>** — <one-sentence definition>. Right
category, or is it <adjacent cut>?

**2. Your critical requirements.** Everything the solution must have. Write them in your own words,
in any order — I'll organise them.

**3. Your non-critical requirements.** Anything you'd like but could live without.

**Or skip 2 and 3** — say "go ahead" and I'll score the field against IDC's most heavily weighted
criteria for this market and flag every assumption.
```

On this path the response is still short: header, headline, ledger with stages 1–6 `Outstanding` (stage 1 provisional), the stage 1 body, the form, Sources, disclaimer. No shortlist and no Recommendations — the form is the next move.

## Uploaded requirements

Where the tech leader uploads an RFI, requirements list or spreadsheet, parse it first and let it **pre-answer the card**: pre-select the market it points to, and where it already carries the requirements, replace questions 2 and 3 with a single confirmation question naming how many critical and non-critical you extracted, offering `Looks right` or `I have changes`. The card still comes first and still renders nothing before it.

Keep their content and IDC's visibly separate wherever the two appear together. Requirements with no catalog match still belong in the stage 2 table, marked unscored — they shape the RFP even when they cannot shape the ranking. Uploaded content is never treated as IDC data (Rule 4).

**When an upload doesn't work.** Four failures. In every case say what happened, say what to do about it, and fall back to the full card — never fail silently, never guess at content you could not read, and never carry on as though requirements had been captured.

- **It wouldn't parse.** Say the file couldn't be read, name it, and offer the two ways forward: re-save in a supported format and re-upload, or answer the questions instead. If it is scanned or image-only, say that is the likely reason.
- **Unsupported format.** Name the formats that work (Word, Excel, CSV, PDF, plain text) and ask for one. Do not attempt to read a format you cannot.
- **Too large.** Ask for the requirements section rather than the whole document.
- **It parsed, but there is too little usable content.** The file opened, but nothing in it maps to a requirement. Say what you did and did not find, pre-select only what genuinely came through, and ask the rest. Do not pad the table with inferences to make the upload look successful.

Where an upload fails, stage 2 reflects only what was actually captured. Never mark it Completed on a failed upload.
