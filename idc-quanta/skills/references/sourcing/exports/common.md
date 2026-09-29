# Exports — shared rules

Read with the one artifact spec you are building: `references/sourcing/exports/rfp.md` or `references/sourcing/exports/negotiation-guide.md`. **These are the only two artifacts this skill exports.** The shortlist (stage 3) and the comparison (stage 4) are chat-only — this skill does not define a file export for either, on the menu or on an explicit request. If a tech leader asks for the shortlist or the comparison as a spreadsheet or a slide, say plainly that isn't something this skill produces, and offer the RFP or the negotiation guide instead where one of those actually fits what they're after.

| Artifact | Stage | Format | Built |
|---|---|---|---|
| RFP + vendor response template | 5 | **Word** + **XLSX** | Picked from the menu, or asked for directly |
| Negotiation guide | 6 | **PowerPoint (PPTX)**, or PDF to forward | Picked from the menu, or asked for directly |

Offer PDF where the file goes into a deck or to someone who should not edit it. Never silently substitute CSV for XLSX.

## How exports work

- **The turn-3 menu is the only place the route offers a file, and no stage body offers one.** An explicit unprompted request ("send me that as a spreadsheet") is always honoured for the RFP or the negotiation guide, whatever turn it lands on — not for the shortlist or the comparison, which this skill never turns into a file.
- **Nothing is produced speculatively.** Neither of these two files is generated until it's picked from the menu or asked for directly.
- **Fidelity is the hard rule: the file matches what the tech leader saw and approved in chat, exactly.** Same vendor count, same ranking, same scores, same tiers, same requirements. If the file needs to differ — a wider vendor set, extra columns — say so in chat first and let them approve that version.
- **Fidelity outranks the tie-break rule.** If the approved shortlist's tied block that feeds the RFP's invited vendor set is not in capability-coverage order — it predates that rule, or the tech leader reordered it — carry the approved order into the file and note the discrepancy rather than silently re-sorting a ranking they signed off. Offer to re-order and reissue.
- **Rebuild is always an explicit action.** Never silently regenerate when an upstream stage changes: mark the stage Outstanding, say which change put it behind, and wait. For an RFP already sent, say plainly a version may be in vendors' hands and offer an addendum as the alternative to a reissue.

## Building the file

Use the session's document skills — the docx skill for Word, the xlsx skill for spreadsheets, the pptx skill for PowerPoint, the pdf skill for PDF.

**Neither file carries IDC branding — no logo, no IDC visual identity, no styling pulled from the IDC brand guidelines skill.** Clean, professional, unbranded formatting only: consistent heading and slide-title styles, one font for body and one for headings, page or slide numbers, consistent table formatting. The RFP reaches vendors who are not IDC subscribers, and the negotiation guide is built the same unbranded way for consistency. The disclaimer and permissions statement are plain text, not a styled letterhead or title-slide graphic.

## Every artifact carries these

Non-negotiable across both files, the response template included. A file missing any of them is not finished.

1. **The disclaimer as the first element**, verbatim from `SKILL.md`. In chat the disclaimer closes; in a file it opens. One per file, never both positions.
2. **A title block** naming the artifact, the confirmed market with its constraints, and the organization it was prepared for.
3. **A generation date and the data vintage it reflects** — the MarketScape edition year (where the Tech Leader data carries it) and the target company size behind the tiers. These are different dates and both matter: a file generated today can rest on a 2024 edition.
4. **The citations, surviving into the file** — inline bracketed numbers in the content and a **Sources** section closing it, using the unlinked Class 1 and Class 3 forms in Rule 3a (`references/sourcing/rules-sourcing.md`). A citation that exists only in chat is an incomplete artifact.
5. **A methodology note**, on every file presenting a score, rank or rating — all of them except the vendor response template, whose rows carry no IDC figures. Short, plain and specific to what the file shows: how the score was calculated (a weighted match against the stated requirements, tiered by importance), that the ranking is deterministic and reproducible against unchanged inputs, that ties were ordered by capability coverage rather than alphabetically, and that scores are relative to the tech leader's requirement set rather than a measure of overall product quality.
6. **A version-and-basis block**, so the tech leader can tell which state of the engagement the file reflects: the market as confirmed, the requirement set it was built on (counts of critical and non-critical, and any exclusions applied), the vendor field size, and the date. When a later version is produced, say which basis changed. If they ask whether a downloaded file is current, answer from this block — name the basis the file carries and the basis the engagement is now on, and offer an updated version rather than implying the old file is wrong.
7. **Customer content kept visibly separate from IDC content.** Label the tech leader's own uploaded RFI, requirements or terms as customer-supplied and IDC's ratings, tiers and narrative as IDC-sourced. A reader must never have to guess which is which.
8. **No reproduction of IDC proprietary research beyond what citing it requires.** Quote and cite; do not rebuild a MarketScape figure, its vendor-assessment tables or its narrative wholesale inside a generated file. This matters most for the RFP, which reaches vendors who are not subscribers.
9. **A permissions statement**, separate from the disclaimer, with the disclaimer at the front. Use the Rule 12 routing line in `references/rules.md`, verbatim:

   > External use of IDC figures, quotes, or MarketScape positioning requires prior written permission from IDC. For citation and external-use requests, contact permissions@idc.com.

   Never construct, shorten or substitute a different contact or URL.

## Generation guardrails

Apply when building any artifact, not only the RFP and the negotiation guide.

- **Never let the artifact refer to itself, its own reasoning or how it was generated.** A line like "this sourcing exercise proceeds in the closest available catalog market" belongs in chat, never in a file a vendor or any third party might read. Share reasoning with the tech leader in conversation; the file carries only the substance.
- **Every stated fact ties to a specific source.** Where the data has nothing for a given point, say so plainly ("not available for this vendor") rather than filling the gap with language generic enough to fit any vendor or market. A negotiation platitude or a piece of procurement boilerplate dressed up as specific guidance fails this rule — insert nothing the tech leader did not state and the data did not support.
- **Content the tech leader shared for their own use never crosses into a vendor-facing file.** The negotiation guide's watch-outs and tactics content is the clearest case, but the rule is general: anything scoped to the buyer's internal use stays out of the RFP or any other document reaching vendors, even within the same engagement.

## When an export fails

- **The file could not be produced or downloaded:** "We weren't able to download your document. Please try again." Offer a retry, then IDC support. Never present a partial file as complete.
- **The platform reports it generated but could not be saved:** "Your artifact was generated but couldn't be saved to Artifacts. Export it now to avoid losing it." Say it at the moment it happens and press the export — the file in their hands is what survives a save failure. Then say the save can be retried, and IDC support if it persists.
- **The platform reports a new version could not be saved:** "Your changes couldn't be saved. Your previous version is still available in Artifacts." Say the save can be retried, and offer to export the current state first if it keeps failing.
- **The platform reports the artifact predates refresh support:** "This artifact can't be refreshed — it was generated before data refresh was supported. Generate a new artifact to get the latest IDC data." Offer to build a fresh one.

Those three platform-reported cases are triggered by what the platform surfaces, not by anything the skill detects. Relay their wording as written, and never assert on your own account that a save succeeded or failed or that a prior version is retrievable.

**Content that could not be built** — a shortlist that would not generate from confirmed requirements — is the stage-3 failure in `references/sourcing/sourcing-core.md`, not an export failure. Never produce an export from content the route could not produce.

## Refreshing an artifact

Re-run the stage's workflow against the current Tech Leader data. Then say plainly which happened:

- **The data moved.** Produce the new version with its basis block updated and say what changed. Changed Tech Leader data re-bases the shortlist, so this is an upstream change: **mark every downstream stage that already ran back to `Outstanding`**, name the refresh as the change that did it, and do not treat a comparison, RFP or guide built on the old basis as still standing. Rebuild each only on its own explicit instruction.
- **Nothing material changed:** "Your artifact is already up to date — no new data has been published since it was last generated." Say that rather than returning an identical file.
- **The data is temporarily unavailable:** "We weren't able to refresh this artifact — the underlying data is temporarily unavailable. Your current version has been preserved."
- **It cannot be refreshed at all** because it predates refresh support — the platform-reported case above.

**A refresh of an RFP already sent is not a routine rebuild.** Say plainly a version may be with vendors, offer an addendum as the alternative to a reissue, and wait for them to choose. A refresh request is not permission to skip that warning. Never describe a refresh you did not run.

## Outside the skill's control

This skill cannot store, version or entitlement-check a file. Never tell a tech leader an artifact is stored, versioned or entitlement-checked: saving to a library, persistent version history (the version-and-basis block identifies a file, but the skill keeps no library), entitlement checks at generation or download, share links and retention of uploaded documents are all outside it.

Where a tech leader asks about any of these, say it is handled by the platform rather than by this response, and do not assert that it happened.
