# Stack


## Business / Initiative
**Agentic Meta Ads** — an agentic system that manages and optimises Meta Ads campaigns across every type of engagement the owner runs.


## Products / Services / Responsibilities
The mix depends on the situation. In every case the job is managing Meta Ads campaigns end to end:
- **Client campaigns** — running Meta Ads for clients, usually lead generation
- **Own ecom** — running Meta Ads for own products when relevant
- **Creative testing** — testing ad creatives to find winners
- **Reporting** — performance reporting to clients


## Daily Tools
| Tool | Use | Status |
|------|-----|--------|
| Meta Ads Manager | Build, run, optimise campaigns | Live (manual access) |
| Meta Business Manager | Accounts, pages, pixels, permissions | Live (manual access) |
| Google Sheets | Lead destination and tracking | Live |
| WhatsApp | Client and crew communication | Live |
| Meta Ads MCP (official, mcp.facebook.com/ads) | Read/write access to own ad accounts: reporting, campaign management, catalogs, signal diagnostics | Not connected — preferred route (replaces raw API token setup) |


## MCP Servers Connected
- Notion — docs and databases
- Google Drive — files (incl. Sheets access via Drive)
- Google Calendar — scheduling
- Airtable — structured data
- Canva — ad creative design
- Adobe for creativity — image/video editing for creatives

Official Meta Ads MCP exists (launched 2026-04-29) but is not connected yet. Setup: authorise the ad account at developers.facebook.com/docs/ads-ai-connectors, then add mcp.facebook.com/ads as a custom connector in Claude settings. It covers own ad accounts only — not the Ad Library.




## Not Accessible
- **Andromeda** (Meta's ad delivery engine) — internal, no external access.
- **Ads Manager AI assistant** — closed, no external access.
- **Ad Library for Morocco** — no official connector; the API covers commercial ads only for EU/UK delivery. Third-party scrapers exist but may breach Meta's terms — owner decision, not used by default. Benchmark = Hafsa's manual captures (see blueprints/client-strategy.md).
