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
| Meta Marketing API (own app "Agentic Ads Hafsa") | Read + prepare campaigns on the main ad account only | Live 2026-09-30. API v26.0. Token in .env, expires 2026-11-29 (renew via Access Token Debugger → Extend) |
| Meta Ads MCP (official, mcp.facebook.com/ads) | Own ad accounts: reporting, campaign management, catalogs, signals. Also Ad Library search | Connected 2026-09-30. Write actions only with Hafsa's approval |


## MCP Servers Connected
- Notion — docs and databases
- Google Drive — files (incl. Sheets access via Drive)
- Google Calendar — scheduling
- Airtable — structured data
- Canva — ad creative design
- Adobe for creativity — image/video editing for creatives

Meta Ads MCP connected 2026-09-30. See live/state.md for which ad accounts have it enabled.
**Ad Library search works for Morocco** (verified 2026-09-30: country=MA, "implant dentaire", 24 active ads). Returns page name, start date, headline, and snapshot link. It does not return the video itself.




## Not Accessible
- **Andromeda** (Meta's ad delivery engine) — internal, no external access.
- **Ads Manager AI assistant** — closed, no external access.
- **Video content of competitor ads**: I can't watch videos. For hooks, visuals and voice-over, Hafsa sends screenshots of key moments or a transcript.
