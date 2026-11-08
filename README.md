# Yandex Metrica MCP by MCPKit

**English** · [Русский](README_RU.md)

Ask ChatGPT about your website traffic, acquisition channels and conversions using data from Yandex Metrica. A hosted Model Context Protocol (MCP) service for marketers, web analysts, SEO specialists, agencies and business owners.

**Currently free to use. Three MCP tools with command details loaded on demand. No coding or local server setup.**

**[Sign up for MCPKit](https://mcpkit.ru/mcp-yandex-metrika)** — choose **Регистрация** (Register) on the website.  
[Connection guide and first report](https://mcpkit.ru/mcp-yandex-metrika/instructions/connect)

This repository contains product information and usage examples for the cloud service. Server source code is not distributed here.

## Understand what happens on your website

Start with a weekly overview, ask which channels changed, then investigate landing pages or devices. You can refine the question in the same conversation instead of manually rebuilding each report.

- **Traffic reports:** visits, visitors, bounce rate, page depth and visit duration.
- **Acquisition and landing pages:** explore traffic sources and pages where visits begin.
- **Goals:** inspect configured goals and their recorded achievements.
- **Period comparisons:** compare two periods with absolute and percentage changes.
- **Multiple accounts:** find available counters across connected Yandex accounts.
- **Deeper diagnostics:** inspect bounded summaries of visitor paths and events through Logs API.

The current service is **read-only for analytics data and counter settings**: it does not create or edit counters or goals. Logs diagnostics may create and clean up temporary data exports.

## Three tools, details on demand

MCPKit exposes just three MCP tools: `tool_list`, `tool_help`, and `tool_execute`. Your AI can request the command catalog, load the detailed instructions for the command it needs, then run it.

The full schemas for every command are not included in the initial tool definitions. This keeps the initial context footprint small, including when you are discussing something else. Catalogs, help and results still use tokens when requested; actual savings depend on the AI client and conversation.


## Try these requests in ChatGPT

These example prompts use supported reports and diagnostics. Choose a connected counter and an existing goal when needed; they are not customer results.

| Your task | Example prompt |
| --- | --- |
| Find a website | “Show my available Yandex Metrica counters with their websites and accounts.” |
| Weekly overview | “Show visits, visitors and bounce rate by day for the last completed week.” |
| Explain a change | “Compare organic traffic for the last two completed weeks. Which landing pages account for the largest decline?” |
| Channel performance | “Compare traffic sources by visits and achievements of the enquiry goal.” |
| Mobile experience | “Compare mobile and desktop traffic by bounce rate and conversion rate for this goal.” |
| Visitor paths | “For the last three completed days, show common visitor paths and behavior associated with goal X.” |

For a landing-page review, first find pages with substantial traffic, then compare goal achievements and changes between periods. The AI can suggest explanations to investigate; the reports do not establish causation by themselves.

## Connect without programming

1. [Register or sign in to MCPKit](https://mcpkit.ru/mcp-yandex-metrika). The same account works with Direct and Wordstat.
2. In the [Metrica dashboard](https://mcpkit.ru/mcp-yandex-metrika/panel), connect a Yandex account that has access to your counters.
3. Copy the server URL from the dashboard. Add a custom MCP connection in ChatGPT, choose **OAuth**, sign in to MCPKit and authorize access.
4. Select the connection in your chat and ask: **“Show my Yandex Metrica counters.”** Then request a report for your counter.

**MCP server URL:** `https://mcpkit.ru/mcp-yandex-metrika/mcp`

You need an AI client/account that supports adding remote MCP servers with OAuth. ChatGPT is the primary documented client; other compatible clients may require different setup.

[Follow the illustrated connection guide](https://mcpkit.ru/mcp-yandex-metrika/instructions/connect) (Russian).

## Availability and limits

MCPKit access is currently free, as stated on the [service website](https://mcpkit.ru/mcp-yandex-metrika). Any AI-client subscription is separate.

Reports use data available to your connected accounts. With several accounts, specify which account and counter to use. Yandex API quotas, field compatibility and sampling rules apply; the service reports sampling when present.

Standard reports are paginated, with up to 100 rows per request. Logs diagnostics cover up to 30 days within processing limits and return compact results, not unrestricted raw exports. Advertising traffic is not necessarily all from Yandex Direct.
## One MCPKit account, three services

Register once to use all three cloud services. Each has its own settings and a separate MCP connection:

| Service | What you can do |
| --- | --- |
| [Yandex Direct](https://mcpkit.ru/mcp-yandex-direct) | Analyze advertising and manage campaigns |
| [Yandex Metrica](https://mcpkit.ru/mcp-yandex-metrika) | Explore website traffic and conversions |
| [Yandex Wordstat](https://mcpkit.ru/mcp-wordstat) | Research keywords, demand and seasonality |

Explore demand with Wordstat, work on advertising with Direct, and assess website performance with Metrica. Connect the services you need; this is not an automatic cross-service workflow.

**[Get your first website report with MCPKit](https://mcpkit.ru/mcp-yandex-metrika)**

