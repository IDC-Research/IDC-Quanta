# Citations

Read this when writing a Sources section or a table source line — that is, on any response that renders a body. Rule 3 in `references/rules.md` points here and this file is its full text. No other file in the package states citation rules; `references/output-format.md` points here rather than restating them.

## Rule 3. Use inline bracketed citations; collect sources before the disclaimer.

Every figure, table, or narrative claim drawn from an IDC tool call is tagged with an inline bracketed number — [1], [2], [3], and so on — placed immediately after the claim it supports. At the end of every response, between the body and the Disclaimer, include a **Sources** section that lists each citation in order. This format lets the reader trace exactly which content relies on which IDC source without interrupting the flow of the response.

**Inline placement:** Add the citation directly after the sentence it supports.

**The `##` headline carries no citation.** It leads with a figure that the Evidence block beneath it states and cites, so a bracketed number in the headline duplicates that citation and reads badly. Every figure in the headline must appear, cited, in the body — a headline figure with no cited counterpart below it is an uncited figure and fails this rule. Rule 13 applies to the headline in full: it is the most-read sentence in the response.

**Tables and figures** carry their title above and their source below, the same way a generated chart does. Put a descriptive title on the line above the table or figure, and a source line directly beneath it:

```
**Worldwide [category] Market Share, [period]**

| Vendor | Share % |
|---|---|
| Vendor A | 38.0% |

Source: IDC's [source name] [1]
```

The source line names the IDC source and ends with the citation number that ties it to the Sources section. Do not place a bare citation number alone beneath a table.

**The only date in a citation is the source's own publication date** — month and year for a research document, year for a data product, both as the connector returns them. Do not add an edition, period or data-vintage label to a source line or a Sources entry, and never compose one from a profile name, a dataset name or an identifier. The period the figures cover belongs in the headline and the table itself, not in the citation. A tracker's edition label (`1H25`, `3Q25`) is not returned by the connector, so it never appears in a citation.

Use the same number for repeated references to the same source. Numbering runs as high as the response requires.

**Quotations must match their source.** Any IDC wording reproduced as a quotation is checked against the retrieved text before use, reproduced exactly as returned, and attributed only to what the source names. Do not join separated passages, trim in a way that changes the sense, or quote text the connector did not return.

**Every piece of IDC content used in a response — data, research, or documents — must be cited.** Assign a distinct number to each IDC source, and make sure every number used in the body has a corresponding entry in the Sources section. No IDC content goes uncited.

**Sources section (required on every response that renders a body, placed before the Disclaimer).** The turns listed under "The exempt turns" in `SKILL.md` carry no Sources section, because they cite nothing. Two forms. Which one an entry takes depends on what the source is, not on which route is running:

```
**Sources**
[1] [<document title>](<live IDC URL>), Doc #<document number>, <Month> <Year>
[2] [IDC <data product name>](<live IDC URL>), <Year>
```

**Form 1, research documents.** Every IDC study, presentation, MarketScape, FutureScape, Perspective, Link, Quick Take, Vendor Profile or other document returned by document search.

- **Title** — the `title` string the connector returns, reproduced verbatim and hyperlinked. Never compose, paraphrase or infer one.
- **Doc #** — the `document_number` exactly as returned, including its country prefix, written as `Doc #US53665725`. Never reformat it, strip the prefix or invent one.
- **Month and year** — from the `published_date` the connector returns, written as the month name and the year (`2026-03-26` becomes `March 2026`).

Example: `[1] [Worldwide Cybersecurity Software Forecast, 2026–2030](https://my.idc.com/getdoc.jsp?containerId=US53665725&pageType=PRINTFRIENDLY), Doc #US53665725, March 2026`

**Form 2, data products.** Trackers, Spending Guides, Black Book and any other library behind a structured-data query.

- **Name** — the `library_name` the data-product catalogue returns, reproduced verbatim and hyperlinked. It already carries the `IDC` prefix and the frequency for most trackers, so nothing is composed. Where it does not begin with `IDC`, add `IDC ` to the front and change nothing else. Where it carries no frequency word, do not invent one.
- **Year** — the publication year from the catalogue entry's `published_date`.
- No document number and no month on a data product, because the catalogue's own identifier is a product number rather than a document number.

Examples: `[2] [IDC Semiannual Software Tracker](https://idctracker.com/technology/WW_SW_TRK/info), 2025` and `[3] [IDC Worldwide Security Spending Guide](<live IDC URL>), 2026`

**Both forms:**

- **Link, always.** A live IDC URL embedded as a markdown hyperlink on the title or product name. Documents carry `document_url` in the search result; data products carry `library_url` in the data-product catalogue. A structured-data query itself returns no URL, so when tracker or spending guide figures came from one, make one data-product search for that library to capture its name, link and publication year together (`references/mcp-playbook.md`, Citation). Keep a captured URL even after retrieving a document's full body, which returns neither URL nor title. Use only URLs the connector returned this session, whatever host they point to — `my.idc.com` and `idctracker.com` are both normal — and never construct, guess or recall one.
- Use the same number for repeated references to the same source. Numbering runs as high as the response requires.

Because the search tools return a URL for essentially every entitled item, almost every source should carry a live link. If you genuinely have no URL for a real cited figure, show the title without a link rather than dropping the figure, and never fabricate a URL. If a number cannot be tied to an MCP response, do not include the number.

IDC Links, Quick Takes, Vendor Profiles, and Executive Snapshots are full research documents: cite them in Form 1 — never by a bare descriptor. The descriptor form is a last resort only for a document that genuinely returns no title; in that case use a short plain descriptor (not a title in quotes) with its link, document number and date when present, for example `[2] [IDC Link](live IDC URL), Doc #US53012325, May 2025 — Quick Take on the Palo Alto / CyberArk deal`. Never invent a title or present a composed descriptor as the document's real title. Titles come from the search result, reproduced verbatim; retrieving a document's full body returns content with no title.

**MarketScape content is cited as a document on both routes.** A MarketScape is an ordinary research document to document search: it returns a verbatim title, a document number, a publication date and a live URL, so it takes Form 1. Where MarketScape positioning instead reached the response through the Tech Leader tools, which return neither title nor URL, resolve it to its document before citing it: one document search limited to the IDC MarketScape content group, using the market wording and edition year from the vendor narrative, then a second search on the market's catalog name and that year if the first returns no confirmed match. Use the returned title, document number, date and URL. Never compose a MarketScape title or construct its URL. Two cases fall back to an unlinked form: the Tech Leader package, where no document search exists, and a lookup that returns no confirmed match after both searches. The fallback is written exactly as:

```
[n] IDC MarketScape assessment, <Market name> — via IDC Tech Leader
```

It is reproduced here so it is available on either route; `references/sourcing/rules-sourcing.md` carries the same form as Class 1 for the sourcing route. Attempt the resolution first in the Full package — an unresolved tier is a last resort, not a shortcut — and say nothing to the user about the lookup either way.

On the sourcing route, Tech Leader dataset content returns no titles or URLs, so it uses the unlinked Class 3 forms in Rule 3a. That is not a missing link.

## Link and attribution rules

These sit with the citation forms rather than with the voice guide:

- **A live link wherever the connector returned a URL.** Markdown hyperlink in chat, an embedded clickable hyperlink in an exported file — never flattened to plain text. A missing link is acceptable; a wrong one is not.
- **Tracker profiles are revised, and the most recent profile is authoritative.** Cite the current one.
- **A synthesizing or directional comment that follows from IDC sources already cited in the response needs no separate citation**, but never present it as a new IDC finding or attribute it to an uncited "IDC analyst view". Where a competitive or directional claim rests on no IDC source, do not attribute it to IDC at all.
- **Traceability is the point.** Every citation exists so the reader can open the source and check the claim, which is why a composed title, a guessed URL or an uncited figure fails even when it looks right.
