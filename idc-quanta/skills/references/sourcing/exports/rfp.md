# RFP (Word) and vendor response template (XLSX)

Read with `references/sourcing/exports/common.md`, whose mandatory elements and generation guardrails all apply. Two files, produced together.

## Two shapes — ask which

They are not the same document. Ask when the tech leader gives the go-ahead, or infer from what they said and state your reading.

- **Lightweight RFP** — typically 3–5 pages: purpose and scope, the requirements table, evaluation basis, submission instructions, assumptions and placeholders, Sources. For a focused or fast-moving selection, a small vendor set, or a tech leader who wants something they can send this week. It carries every common element; it simply carries less body.
- **Full formal RFP** — the complete 13-section structure below. Where procurement requires a formal document, where the purchase is large or regulated, or where the long form is asked for.

Where nothing indicates a preference, offer the lightweight version and say the full formal structure is available. It is the less wasteful default.

- **Where the lightweight shape is used, name what was left out.** One line in the document, not only in chat, naming which sections of the full formal structure were deliberately dropped and why — for example, no vendor company-profile appendix, no references appendix, no formal Q&A log, because they add process weight better suited to a broader tender than a quick request to one or two finalists. A shorter document should never read as an accidental omission.

## The RFP document

- **Built on the tech leader's supplied template where one exists; otherwise IDC's default structure — and the document states which was used.** Put that statement in the document, not only in chat.
- **Carries the standing stages 1–3 without re-asking for any of them:** the confirmed market and its definition, the full requirements table including every requirement marked "not in IDC's requirement catalog", and the approved shortlist as the invited vendor set.
- **Any catalog requirement for the market the tech leader never discussed or prioritized is surfaced, not silently resolved.** Put the choice to them directly: include it at a lower default priority, leave it as an open question for vendors, or exclude it from this RFP entirely. Neither silently omitting it nor silently including it at an assumed priority is acceptable.
- **A stated need with no exact catalog match, only a generic proxy, is named as a substitution before generating.** "There's no NetSuite-specific requirement in the catalog, I've mapped this to the general API-integration requirement instead" is said to the tech leader, not silently treated as equivalent to what they actually asked for.
- **Evaluation-criteria weightings are validated to sum to 100% before the document generates.** If Functionality, Cost and Support add up to 90%, flag the discrepancy and ask how to close the gap rather than generating a document with a broken table.
- **No generic procurement philosophy is stated as the tech leader's own position.** A line like "we prefer cloud-based solutions to maximize flexibility" only belongs in the document if the tech leader said something to that effect — never because boilerplate language happened to be sitting in a template.
- **The invited vendor list names vendors and products — not their tiers, scores or coverage denominators.** The RFP reaches vendors who are not IDC subscribers, and printing each recipient's tier and score inside a document sent to all of them is both a disclosure of subscriber content and commercially poor. Name the invited set in the approved order, state in the document that IDC's ratings informed the selection and are held by the issuer, and keep the ratings out of it — they stay in chat with the tech leader, since the shortlist itself is never exported as a file.
- **The RFP document itself carries no methodology note.** It presents no IDC score, rank or rating to a vendor audience, so `common.md`'s methodology-note requirement does not apply to it, the same as the response template.
- **A numeric threshold you inferred from a qualitative requirement is not stated to vendors as a specification.** Ask vendors to report their actual figure instead, and record the inferred threshold in the assumptions section.
- **Default section order** when IDC's structure is used: (1) disclaimer; (2) title and issuing organization; (3) purpose and scope, with the confirmed market definition; (4) background and current environment, only as far as supplied; (5) scope of work and functional requirements; (6) technical requirements — integration, deployment, security and certifications; (7) company and vendor requirements; (8) mandatory exclusions; (9) evaluation criteria and weighting, reflecting the critical / non-critical split; (10) submission instructions — due date, contact, format, questions deadline; (11) commercial and contractual asks; (12) assumptions and placeholders; (13) citation appendix and Sources.
- **Assumptions and placeholders are stated in the document, in one enumerated place.** Anywhere requirements were inferred rather than stated, anywhere a detail was left to fill, it is listed — the vendor receiving this needs the same clarity a returning tech leader would. A placeholder is written as an obvious placeholder, never as plausible invented content.
- **The generation message states which sections came directly from the tech leader and which stay their own responsibility from here.** Running the vendor Q&A rounds, collecting references, negotiating a best and final offer are the tech leader's own next steps, not something this document carries them through — say so plainly at the point of generating, not only if asked.
- **The citation appendix** covers the requirements ranking that shaped the RFP, in the Rule 3a forms.
- **Never overwrite a prior RFP.** A new version is a new file with its version-and-basis block updated.

## The vendor response template

A separate XLSX structured on the same requirements so answers come back comparable: one row per requirement carrying the requirement text, its type and its importance, plus empty columns for the vendor's response, their comments, and the release or module that delivers it. The response column carries a three-state schema — capability included in the proposed application, capability delivered through a partner (with a note on which partner), or capability on the vendor's roadmap within 18 months — alongside the overall Full / Partial / No support label, so a vendor can complete it directly without restructuring the sheet. Add a sheet for commercial response where the RFP asks commercial questions. Lock or protect the requirement columns so the structure survives the round trip, and leave a short instructions block at the top.

It carries the disclaimer, the permissions statement and the title block. It is the one file needing no methodology note, because it presents no IDC score, rank or rating.
