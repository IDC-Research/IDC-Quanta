# Working with IDC Data

Read this before any structured-data work. It covers the practice the connector's own tool descriptions do not: how to choose the right data product, how to resolve the right period, how to capture a citation, and which source wins when two disagree.

This file deliberately does not list the connector's tools. The connector supplies its own tool names, descriptions and schemas at call time, and those are authoritative for what exists, what each tool takes, what order they run in, and any constraint a tool states about itself. Read them and follow them. Where a tool description and this file differ on mechanics, follow the tool description; the guidance below is about practice, not plumbing.

## Discovery: choose from the catalogue

Resolve the entity, market and geography first, then choose the data product.

Prefer the connector's full catalogue listing over its keyword search when deciding which library answers the question. Keyword search over data products ranks a subset of the catalogue, so use it to confirm a candidate rather than to find one. Request the catalogue once and cache it for the session.

Narrow to likely libraries by name and scope using the selection rules in `references/idc-data-landscape.md` before you query, so you are selecting deliberately from the catalogue rather than working through every library in it. **Narrow down first; do not list the datasets of every library.** If a tool description tells you to list datasets for every library returned, do not: list datasets only for the libraries you shortlisted. This is the one exception to following tool descriptions on mechanics. Confirm the user is entitled to a product before promising data from it (Rule 12).

## Period: open the newest, then filter

Select the newest published period for the market, then filter to the period the user asked about inside it. Never anchor to the year named in the question, and never settle for an earlier edition because it looks like a closer match. This applies to every quantitative pull, including a quantitative step inside an otherwise qualitative answer.

Several candidates commonly share the newest period, differing only by the subscriber view they belong to. They are not alternative editions. Take any one carrying the newest period, then confirm the period from the query response itself rather than from the candidate's name, which is not a data-scope signal. Never enumerate these to the user or name one in a response.

## Citation: capture the link at the step that has it

Rule 3 defines the two Sources forms. This section is about where each field comes from, because a citation cannot be assembled from the step that returns the figures.

A structured-data response returns figures and little else. It does not carry a link, a product name or a date, so carry the library's identity forward from the step where you chose it, then make one data-product **search** for that library — the keyword search over data products, not the plain library listing, which returns names and ids only. That search result is what carries everything a data-product citation needs: the `library_name` to cite it by, the `library_url` to link it, and the `published_date` for its year. Make it before writing the Sources section, not after. One call covers both jobs when the same search confirmed the product at the discovery step: capture the three fields there and do not repeat it.

A research document carries its fields in the search result that surfaced it: `title`, `document_number`, `published_date` and `document_url`. Capture all four there, because retrieving the document's full body returns content without any of them. Never rebuild a title from a document's body, and never read a document number off a cover page or a chunk when the search result carries one.

Reproduce a title or product name exactly as the connector returned it. Accept any IDC-owned domain. Use only links the connector returned this session, and never construct, guess or recall one.

## Precedence: data outranks documents

For any share, size or growth figure, the data product is the authoritative source over a research document covering the same scope (Rule 8). Where a figure rests on research documents rather than data, apply the hierarchy as the rules actually state it: Rule 5's hard floor puts full research above blogs, abstracts, press releases and marketing material; Rule 6 relevancy-weights framework documents; and Rule 7 decides the axis — a quantity ranks by recency, a judgment ranks by the document that most directly addresses the question rather than the newest one. There is no general ladder by document series, so do not rank a MarketScape above a Market Note on series alone; rank on the axis the claim sits on.
