# Blueprint — Client Strategy

**Goal:** For each client or project, produce a Meta Ads strategy grounded in market research and a competitor benchmark from the Meta Ad Library. The strategy gets the client qualified leads within 3 months and a clear path to scale.

**Equipment:** None. Research and writing — the Architect handles it natively.
**Reference:** references/playbooks/meta-ads-scaling.md (principles), .claude/rules/campaigns.md, .claude/rules/permissions.md, .claude/rules/voice.md


## Required Inputs
1. `live/<client>/brief.md` — a completed copy of templates/client-brief.md. All (R) fields filled, even if "unknown".
2. Ad Library captures in `live/<client>/research/ad-library-raw/` — screenshots or ad links from Hafsa (see Benchmark Sources).

If the brief is missing or any (R) field is blank: list the missing fields and stop. If captures are missing: continue with source 2 and say so in the report.

`<client>` is kebab-case, e.g. `clinique-dentaire-rabat`.


## Benchmark Sources (in order)
Verified 2026-09-29: the Ad Library website returns 403 to automated requests, and the Ad Library API only returns commercial ads delivered in the EU/UK. Moroccan-targeted ads cannot be pulled automatically.

1. **Hafsa's manual captures** (primary). She browses facebook.com/ads/library with country = target country and "All ads", and saves screenshots or ad links per competitor. I read and analyse them.
2. **Web research** on competitors: websites, landing pages, offers, pricing, Instagram/Facebook pages, reviews.
3. **Ad Library API** — only if a competitor also advertises to EU/UK audiences (e.g. France-targeted campaigns) and an API token exists in .env. Ask before calling.

Always state which sources were used.


## Sequence

### Step 1 — Intake
- Create `live/<client>/` with `brief.md`, `README.md` (from templates/client-readme.md), `research/`, `strategy/`.
- Fill README from the brief. Target CPL is marked "proposal" until Hafsa approves.

### Step 2 — Market Research
WebSearch for the niche in the target country:
- Demand and seasonality
- Typical prices and offers
- Customer pain points, desires, objections (reviews, forums, social comments)
- Current Meta features relevant to this campaign type — verify before naming any product feature (Meta changes often)

Save to `live/<client>/research/market-research.md` with sources and dates.

### Step 3 — Competitor Benchmark
For each competitor (3–8), record:
| Field | What to capture |
|---|---|
| Active ads | Count |
| Longest-running ad | Start date, what it shows — long runners are likely winners |
| Formats | Video / image / carousel / UGC mix |
| Hooks and angles | First line or first 3 seconds, main promise |
| Offer and CTA | Discount, free consultation, price shown, CTA button |
| Destination | Instant form / WhatsApp / website |
| Language | FR / Darija / Arabic / EN |

Save to `live/<client>/research/ad-library-benchmark.md` with source and date for each row.

If no competitors are known: find 3–5 candidates by web search and ask Hafsa to confirm before benchmarking.

### Step 4 — Synthesis
In the benchmark file, add:
- **Proven patterns** — what multiple competitors do and keep running
- **Gaps** — angles, offers, formats, or audiences nobody is using
- **Our angle** — how this client wins

### Step 5 — Strategy Document
Write `live/<client>/strategy/<YYYY-MM-DD>-strategy.md` in the client's language, with these sections:
1. **Summary** — 3–5 lines: goal, approach, expected result in 3 months
2. **Objective and KPIs** — target CPL and target cost per qualified lead, derived from lead value and budget. Show the math.
3. **Tracking and lead flow** — pixel/CAPI status, lead destination, form questions (3–5 fields + qualifiers), Sheets feedback loop, speed-to-lead requirement for the client
4. **Campaign structure** — testing vs scaling, number of campaigns/ad sets sized so each can exit learning at this budget
5. **Audiences** — default broad, what to test against it
6. **Creative plan** — angles × formats matrix (5+ angles from Steps 2–4), hooks, production notes (Canva/Adobe or client-made)
7. **Budget split** — testing vs scaling per month (proposal)
8. **3-month roadmap** — Month 1 learn/test, Month 2 consolidate, Month 3 scale, with milestones per month
9. **Scaling rules and kill rules** — from the playbook, adjusted to this client's numbers
10. **Risks** — and what we do if month 1 is off track

Every budget figure, launch, pause, or budget change is labelled **Proposal — needs Hafsa's approval**.

### Step 6 — Report to Hafsa
Short paragraphs in her format (voice.md): what the research found, the recommended strategy in brief, what I advise doing first. List every file created. List open questions.

Update `live/<client>/README.md` next action and `live/state.md`.


## Expected Output
```
live/<client>/
  brief.md
  README.md
  research/market-research.md
  research/ad-library-benchmark.md
  research/ad-library-raw/        (Hafsa's captures)
  strategy/<YYYY-MM-DD>-strategy.md
```


## Failure Handling
- **Brief incomplete** — list missing (R) fields, stop.
- **No Ad Library captures** — benchmark from web research only, say so clearly, recommend Hafsa adds captures and re-run Step 3–4.
- **Web search finds little for the niche/country** — say so, lean on playbook principles and the brief, flag assumptions.
- **Budget too small to exit learning** — say so plainly in the strategy and propose the fix (fewer ad sets, higher-volume optimisation event, or longer timeline).
- **Conflict between brief and research** (e.g. client price far above market) — raise it as a risk, don't hide it.
