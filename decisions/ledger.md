# Decision Ledger


Append-only. Every meaningful call gets logged here.
Format: [YYYY-MM-DD] DECISION: ... | REASONING: ... | CONTEXT: ...


---

[2026-09-29] DECISION: Meta Ads is the only ad platform for now — no Google Ads, TikTok, etc. | REASONING: Established before EA setup — owner directive | CONTEXT: Onboarding, Section 5
[2026-09-29] DECISION: All leads go into Google Sheets | REASONING: Established before EA setup — owner directive | CONTEXT: Onboarding, Section 5
[2026-09-29] DECISION: Budget is set per client and per project — no global budget rule | REASONING: Established before EA setup — owner directive | CONTEXT: Onboarding, Section 5
[2026-09-29] DECISION: Build the client strategy workflow first, weekly client report second | REASONING: Strategy comes before campaigns; Hafsa chose it | CONTEXT: First Build Queue item after onboarding
[2026-09-29] DECISION: Ad Library benchmark uses Hafsa's manual captures as primary source, web research as secondary, Ad Library API only for EU/UK-targeted competitors | REASONING: Verified the Ad Library site returns 403 to automated requests and the API returns commercial ads only for EU/UK delivery — Moroccan ads can't be pulled automatically | CONTEXT: blueprints/client-strategy.md
[2026-09-29] DECISION: Use the official Meta Ads MCP (mcp.facebook.com/ads) as the route to ad account data, instead of a raw Marketing API token in .env | REASONING: Official, covers reporting + management + diagnostics, no custom Equipment needed for data access. Andromeda and the Ads Manager AI assistant have no external access | CONTEXT: Hafsa asked about connecting to Andromeda / Meta's AI; connector not yet authorised
[2026-09-30] DECISION: The Ad Library benchmark now uses the Meta Ads MCP Ad Library search (works for Morocco) as its primary source, with Hafsa's screenshots/links for video content | REASONING: Tested 2026-09-30, country=MA returned active commercial ads. This corrects the 2026-09-29 entry, which predates the connector | CONTEXT: Hafsa asked whether I can analyse active Ad Library videos
[2026-09-30] DECISION: Work only on the main ad account (name and ID in CLAUDE.local.md) — no other ad accounts | REASONING: Owner directive | CONTEXT: Meta Ads connector not yet enabled on this account (Meta rollout); interim routes = manual launch + CSV, or Marketing API via own developer app (pending approval)
[2026-09-30] DECISION: Connect the main ad account through the Marketing API with Hafsa's own developer app ("Agentic Ads Hafsa", development mode, no business portfolio), permissions ads_read + ads_management + pages_show_list only | REASONING: The Meta Ads connector is not enabled for this account (Meta rollout, no manual route). Least privilege: business_management left out so no access to her other Business Managers | CONTEXT: Token verified 2026-09-30, expires 2026-11-29. Campaigns will only ever be created PAUSED
