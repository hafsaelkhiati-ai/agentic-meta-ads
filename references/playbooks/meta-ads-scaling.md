# Meta Ads Scaling Playbook

Reusable principles for lead-gen strategy. Cited by blueprints/client-strategy.md.
*Last verified: 2026-09-29. Meta changes often — re-check anything product-specific before recommending it.*


## 1. Lead Quality Over Volume
- Optimising for raw form fills finds the cheapest completions, not the best prospects. The algorithm needs a downstream signal (qualified lead, booked call, sale).
- Build the feedback loop from day one: leads land in Google Sheets, Hafsa or the client marks them qualified or not, and that status is sent back to Meta (CAPI / offline conversions) once the setup allows it.
- Instant forms: 3–5 fields. Add one or two qualifying questions (budget, timeline, city) when lead quality matters more than volume. "Higher intent" form type trades volume for quality.
- Speed to lead: contacting within minutes changes the qualified rate more than most ad tweaks. Put this in every strategy as a client-side requirement.


## 2. Learning Phase
- An ad set typically exits learning after about 50 results in the week after its last significant edit. Below that it stays "Learning Limited".
- Implication for small budgets: fewer ad sets, not more. Consolidate so each one can reach enough results. If budget can't reach ~50 leads/week, optimise for a slightly higher-volume event or accept a longer learning period — state which in the strategy.
- Bundle edits. Every significant change (budget jump, targeting, new creative in the ad set, optimisation event) can reset learning.


## 3. Structure
- **Testing** — new creatives and angles, controlled budget, clear kill rules.
- **Scaling** — proven winners only, most of the budget.
- Default audience approach: broad targeting (Advantage+ audience) with the right geography. Creative does the targeting. Use manual interests or lookalikes only as a test against broad, not as the default.


## 4. Creative
- Creative is the main lever. Plan angles × formats, not single ads.
- Angles come from customer pain points, desires, objections, and gaps in the competitor benchmark.
- Short vertical video (9:16) first, then static and carousel. UGC-style often beats polished for lead gen.
- Fatigue signals: frequency rising, CTR falling, CPL rising for the same ad over 7–14 days. Answer with fresh creative, not budget cuts.
- A competitor ad running for a long time is usually profitable. Study its hook, offer, and format.


## 5. Scaling
- **Vertical:** raise budget on winning ad sets gradually (about 20% every few days when CPL holds). Big jumps reset learning.
- **Horizontal:** duplicate winners into new angles, formats, or geographies.
- Scale only on stable cost per *qualified* lead, never on CPL alone.
- Every budget change is a proposal for Hafsa's approval (.claude/rules/permissions.md).


## 6. Kill Rules (defaults — adjust per client)
- Ad spent 2× target CPL with 0 leads → propose pausing.
- Ad set CPL above 1.5× target after exiting learning → propose fixing creative or pausing.
- Qualified rate below half the account average → review form and angle before spending more.


## 7. The 3-Month Window
Clients expect qualified leads within 3 months max.
- **Month 1 — Learn and test:** tracking in place, 3–5 angles tested, first CPL and qualified-rate baseline.
- **Month 2 — Consolidate:** cut losers, feed winners, iterate on winning angles, improve form qualification.
- **Month 3 — Scale:** move budget to proven campaigns, expand horizontally, hit the client's lead target.
Flag early (end of month 1) if the account is off track.
