# IDC Quanta

IDC Quanta brings IDC market intelligence and technology sourcing into Claude. It answers IT market questions with live data from IDC Trackers, IDC Spending Guides, and IDC research documents, and it guides technology buyers from a need to a purchase decision using IDC vendor ratings and commercial data. It cites every figure back to its IDC source and does not answer these questions from Claude's general knowledge.

IDC Quanta is published by IDC (International Data Corporation). An active IDC subscription is required to use it.

## Packages

IDC offers this plugin in three packages. Your IDC subscription decides which one you have, and the plugin adjusts automatically.

- **IDC Quanta:** market intelligence
- **IDC Tech Leader:** technology sourcing
- **Both:** market intelligence and technology sourcing

If you ask for something outside your package, the plugin tells you it isn't included and does not answer from other sources.

## What it includes

- **IDC Quanta skill.** Tells Claude when to use IDC data, how to choose the right IDC source, how to run a sourcing engagement step by step, and how to format answers with a source line, a confidence rating, inline citations, a Sources list, and the IDC disclaimer.
- **IDC connector.** A remote MCP server at `https://mcp.idc.com/mcp` that gives Claude search and query access to IDC data, research, and Tech Leader vendor ratings.

The plugin works in Claude chat, Cowork, and Claude Code.

## What you can ask: market intelligence

- **Market share and rankings:** "Who leads the cloud IaaS market?" or "How has vendor share changed over the last two years?"
- **Market size and forecasts:** "How big is the security software market?" or "What is the five-year CAGR for AI platforms?"
- **IT spending by industry:** "How much is banking spending on AI?"
- **Vendor positioning:** IDC MarketScape Leaders and how vendors are positioned in a market
- **Competitive intelligence:** competitor strategy, battlecards, early market signals, and deal strategy
- **Emerging technology:** adoption timing, maturity, business impact, and risk
- **Executive and M&A briefings:** market context for boards, investment cases, and acquisition targets
- **IDC research:** "What does IDC say about sovereign cloud?" and citation-ready analyst quotes

## What you can ask: technology sourcing

For a purchase you're making, IDC Quanta works through the decision with you in stages:

1. Resolve your need to an IDC market
2. Define and rank your requirements
3. Build a scored vendor shortlist
4. Compare finalists side by side
5. Build an RFP with a vendor response template
6. Prepare for negotiation

Try "We're replacing our endpoint security vendor. Who should we consider?" or "Build an RFP for our shortlist."

The RFP comes as a Word document and an Excel response template. The negotiation guide comes as a PowerPoint deck or a PDF. Claude builds these files in your session only when you ask for them. Neither file carries IDC branding. File creation uses Claude's built-in document tools in Claude chat and Cowork. In Claude Code, it depends on the document tools available in your setup.

Ask in plain language. You don't need to mention IDC or use a command, though you can also start the skill directly by typing `/` and choosing IDC Quanta. In Claude Code the command is `/idc-quanta:idc-quanta`. Run it on its own to see a list of what you can ask.

## Setup

1. Install the IDC Quanta plugin from the Claude directory.
2. Open the plugin's **Connectors** tab and connect the IDC connector.
3. Sign in with your IDC account when prompted. On Team and Enterprise plans, an Owner may need to add the connector for your organization first.
4. Ask a market question to confirm the connection.

If the connector isn't connected, IDC Quanta tells you it can't reach IDC and asks you to connect it.

## How it works and what data it sends

- When you ask a question, Claude sends search terms and query parameters based on your question (for example, market names, vendor names, industries, regions, time periods, and the requirements you state for a purchase) to the IDC connector at `https://mcp.idc.com/mcp`.
- The connector returns IDC data and research that your IDC subscription entitles you to see. Claude uses those results to write the answer.
- The plugin contacts no service other than the IDC connector.
- The plugin contains only instructions and a connector reference. It runs no local code, scripts, or hooks, downloads nothing at install time, and stores nothing on your device.
- Files you share in the conversation, such as an RFI, are read by Claude in your session and are never sent to the IDC connector. RFP and negotiation files are also created in your session.
- The plugin does not read credentials or files from your computer. You sign in to IDC through the connector's own sign-in flow.

## Privacy

IDC handles data sent to the IDC connector under the [IDC Privacy Policy](https://www.idc.com/about/privacy/).

## Terms of use

IDC Quanta is intended for authorized IDC subscribers. Answers include IDC content that is subject to your IDC subscription agreement. Do not redistribute or publish IDC content in whole or in part without prior written authorization from IDC. To ask what you can share or to request approval, contact IDC Permissions at permissions@idc.com. Answers are generated by AI and may contain errors, so confirm important figures before relying on them. Answers are not professional advice.

## Support

- **Login issues, technical errors, or connector problems:** idc_support@idc.com
- **Subscriptions, billing, account management, or renewals:** customerservice@idc.com

## License

See the LICENSE file in this plugin folder.
