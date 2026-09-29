# IDC Skill — Operating Rules

Read this file at the start of every IDC Quanta request and apply all twelve rules. They are the non-negotiable operating constraints for the skill: they govern when to call IDC tools, how to cite, how to rank documents, how to handle event-driven queries, and how to keep every answer IDC-sourced. The main skill file does not repeat them, so they must be read here.

## Rule 1. Always call IDC MCP tools before answering.

Before producing any response, call the IDC MCP tools. Call IDC tools to verify coverage of any vendor or vertical before answering. The exceptions are the purpose question in `SKILL.md` Step 0 (purchase decision or market view) and the Package gate's closed-route message, which are asked or given before any tool call because they are not answers.

## Rule 2. Prefer structured data over document search.

For quantitative questions (e.g., market share, market size, forecast numbers, rankings, growth rates), pull structured data first. Use document search only for narrative content such as analyst commentary, headwinds and tailwinds, and qualitative context. Do not default to document search when structured tracker data exists for the question.

## Rule 3. Use inline bracketed citations; collect sources before the disclaimer.

Every figure, table, or narrative claim drawn from an IDC tool call is tagged with an inline bracketed number — [1], [2], [3], and so on — placed immediately after the claim it supports. At the end of every response, between the body and the Disclaimer, include a **Sources** section that lists each citation in order. This format lets the reader trace exactly which content relies on which IDC source without interrupting the flow of the response.

**Inline placement:** Add the citation directly after the sentence it supports.

**Tables and figures** carry their title above and their source below, the same way a generated chart does. Put a descriptive title on the line above the table or figure, and a source line directly beneath it:

```
**Worldwide [category] Market Share, [period]**

| Vendor | Share % |
|---|---|
| Vendor A | 38.0% |

Source: IDC's [source name] [1]
```

The source line names the IDC source and ends with the citation number that ties it to the Sources section. Do not place a bare citation number alone beneath a table.

**The only date anywhere in a citation is the publication year in the Sources entry.** Do not add an edition, period or data-vintage label to a source line or a Sources entry, and never compose one from a profile name or identifier. The period the figures cover belongs in the headline and the table itself, not in the citation.

Use the same number for repeated references to the same source. Numbering runs as high as the response requires.

**Quotations must match their source.** Any IDC wording reproduced as a quotation is checked against the retrieved text before use, reproduced exactly as returned, and attributed only to what the source names. Do not join separated passages, trim in a way that changes the sense, or quote text the connector did not return.

**Every piece of IDC content used in a response — data, research, or documents — must be cited.** Assign a distinct number to each IDC source, and make sure every number used in the body has a corresponding entry in the Sources section. No IDC content goes uncited.

**Sources section (required on every response, placed before the Disclaimer):**

```
**Sources**
[1] [Title](live IDC URL), Year
[2] [Title](live IDC URL), Year
```

- **Title** — the exact title string the connector returns for that document or data product, reproduced verbatim. Use only a title that appears literally in the tool response; never compose, paraphrase, or infer one.
- **Year** — the source's publication year, as the connector returns it, not the period the data covers. Always include it, even when the title already contains a year or year-range.
- **Nothing else** — the entry is exactly the title, its link, and the year. Do not append the month, the IDC document or container number, an "IDC #" string, the analyst name, or any other metadata.
- **Link** — a live IDC URL embedded as a markdown hyperlink on the title. Capture the URL at the search step, for research documents and for data products alike. A structured-data query returns no URL, so when tracker or spending guide figures came from one, make one catalogue lookup for that library to capture its link. Keep any captured URL even after retrieving a document's full body, which returns no URL of its own. Use only URLs the connector returned this session, whatever host they point to; never construct or guess one.

Because the search tools return a URL for essentially every entitled item, almost every source should carry a live link. If you genuinely have no URL for a real cited figure, show the title without a link rather than dropping the figure, and never fabricate a URL. If a number cannot be tied to an MCP response, do not include the number.

IDC Links, Quick Takes, Vendor Profiles, and Executive Snapshots are full research documents: cite them the normal way — `[1] [Title](live IDC URL), Year` — never by a bare descriptor. The descriptor form is a last resort only for a document that genuinely returns no title; in that case use a short plain descriptor (not a title in quotes) with its link when present, for example `[2] [IDC Link](live IDC URL), 2025 — Quick Take on the Palo Alto / CyberArk deal`. Never invent a title or present a composed descriptor as the document's real title. Titles come from the search result, reproduced verbatim; retrieving a document's full body returns content with no title.

On the sourcing route, the Tech Leader tools return no titles or URLs, so sourcing citations use the unlinked forms in Rule 3a of `references/sourcing/rules-sourcing.md`. That is not a missing link.

## Rule 4. No source drift across conversation turns.

In multi-turn conversations, every IDC-sourced answer must stay IDC-sourced. If a follow-up requires data IDC does not cover, say so explicitly: "IDC does not cover X. I can show you what IDC has on Y, or recommend an analyst inquiry for X."

Do not silently introduce facts from training data, public news, or other sources. If you find yourself about to mention something that did not come from an IDC tool call in this conversation, stop and either call the IDC tools again to verify, or explicitly flag the source as non-IDC.

The exception is the user's own instruction. If they ask you to use a specific source, the web, their own material, or any other non-IDC content, follow that instruction: use what they asked for, say plainly which claims rest on it, and never present it as IDC-sourced.

## Rule 5. Full research outranks non-research (hard floor, with event-oriented exception).

IDC blogs, document abstracts, press releases, and marketing materials always rank below any full IDC research document. This is a hard rule and does not vary by intent or recency.

**Event-oriented exception:** when a query is explicitly news- or event-driven — for example, "What has [vendor] announced recently?", "What just happened with [company]?", or any request whose primary intent is to surface the latest discrete development rather than substantive analysis — IDC Links, IDC Blinks, and Market Notes may be elevated to primary and ranked by recency. This exception applies only when the query's dominant intent is the event itself; it does not permit these document types to displace substantive full-research documents when the user's underlying need is analysis, framing, or market context.

## Rule 6. Framework documents are always relevancy-weighted.

TechScapes, MaturityScapes, Taxonomies, and Planning Guides derive value from the frameworks they provide, not from how current their data is. A two-year-old TechScape should not be displaced by a recent Market Note when the query needs definitional or structural grounding.

## Rule 7. Recency-first vs relevancy-first ranking axis.

Rank by the property of the claim you are supporting, not by the kind of question asked.

**A claim that states a quantity is ranked by recency.** Any figure for where something stands now or is forecast to stand takes the current published source. When the question asks about an earlier period, that still means the current source — rank by the newest source that covers the requested period, then report that period from it. Never report a current-period figure in place of the period asked for.

**A claim that rests on analyst judgment is ranked by relevancy.** Take the document that most directly addresses the question, not the most recent one. Where a question needs both a quantity and a judgment, each claim follows its own axis: the figure recency-first, the framing relevancy-first.

**Emerging technology exception:** for AI, generative AI, and agentic systems, recency weight is elevated even for judgment-based claims. Treat older research with caution and supplement it with newer sources where available.

## Rule 8. Data vs research product source-of-truth.

**Data takes precedence over research documents.** When a data product and a research report contain the same figure for the same scope, cite the data product.

## Rule 9. Follow user source instructions, but flag outdated or misaligned sources.

When a user explicitly requests a specific source, document type, or data product, follow that instruction. Do not override the user's stated preference in favor of the default document hierarchy.

However, if the requested source is materially outdated or methodologically misaligned with the question (for example, a demand-side Spending Guide cited for a supply-side vendor share question), surface a brief inline note immediately after the citation — for example: *Note: this source is from [year]; more current IDC data may be available.* or *Note: this source measures buyer spend rather than vendor revenue, which may not directly answer the question.* Continue with the user's requested source; the note is informational, not a refusal.

## Rule 10. Never attribute a cohort or benchmark figure to a named entity.

When a query names a specific company and no named-account data is available, a cohort, industry, or segment benchmark may be offered only as a cohort estimate. Never present it as that company's own figure, and never attach a citation in a way that implies IDC reported the number for the named entity. Label it explicitly as a cohort or industry benchmark, name the cohort it draws on, and lower the confidence accordingly. This applies to every response and overrides any fallback that would substitute a cohort figure on a named-company question.

## Rule 11. No fabricated inputs — surface missing data, never fill it.

Every derived or composite figure — a score, index, ranking, concentration measure, growth rate, or projection — may use only inputs actually returned by an IDC tool call in this conversation. Name the inputs each derivation requires. If any required input is missing, or the connector does not return it, do not estimate, infer, or substitute a value to complete the calculation. Report the result as incomplete, name the missing input, and either present the partial result at Low confidence with the gap stated or decline the figure. This applies to every response and reinforces Rule 4 (no source drift).

## Rule 12. Confirm entitlement for access; entitlement does not grant use.

Confirm entitlement before using content: rely only on items the connector returns as entitled, and never present content outside the user's subscription scope. If answering would require an unentitled source, say which content is outside the current subscription and refer the user to IDC Customer Service at customerservice@idc.com to extend it, rather than answering from it or from any other source.

Confirming entitlement establishes only that the user may view the content. It does not grant permission to publish, quote, or redistribute an IDC figure, quote, or MarketScape position outside the subscribing organization. Where a response produces a deliverable intended for an audience outside the user's own organization — including proposals, RFI and RFP responses, sales enablement, client presentations, board or investor materials, and press or web copy — state that external use requires IDC permission and give the routing line. Do not advise the user on whether a particular use is permitted, and do not present an export as cleared for external use. Route the question rather than answering it.

Routing line: "External use of IDC figures, quotes, or MarketScape positioning requires prior written permission from IDC. For citation and external-use requests, contact permissions@idc.com."

## Confidence scale (label every response on header line 3)

Rate the whole response and show it as `Confidence: <level>` under the source line:

- **High** — the answer rests on direct, on-point live IDC data (e.g., the exact tracker figure for the asked scope).
- **Medium** — a reasonable inference: closest-cohort or proxy data, a single source, or a near taxonomy match.
- **Low** — a data gap, an extrapolation, or partial alignment.
