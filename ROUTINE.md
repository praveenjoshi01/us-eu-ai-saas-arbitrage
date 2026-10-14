# Daily routine prompt

Run from the repo root on `main`. State lives in `data/`; the site in `site/` renders it.

## Goal
Build and update conviction in hypotheses about US application-layer AI SaaS that has a structural EU gap and can be built and sold from Ireland. Every run must leave `data/` better informed than it found it, even if no new round appears.

## Steps
1. **Read state.** Load `data/theses.json`, `data/candidates.json` and the last 7 files in `data/runs/`. Do not repeat searches already logged.
2. **Sweep (parallel, one sub-agent per family).** Fetch pages, not just snippets.
   - Funding: Crunchbase News, TechCrunch AI, Superpower Daily tracker, US VC blogs, SEC Form D filings. Window: last 24h, plus a 30-day lookback for clustering.
   - Demand: Product Hunt, Hacker News, Reddit, G2, YC batch lists, job boards.
   - EU side: Dealroom, Crunchbase, LinkedIn, Enterprise Ireland HPSU, EU AI Act and GDPR enforcement news.
3. **Filter** to US, application-layer AI SaaS. Per round record company, one-line product, stage, amount, lead, date, source link. Add to `data/candidates.json`; skip duplicates.
4. **EU check** per new or watched candidate: EU competitors (name, country, funding) and structural EU gap (GDPR/AI Act, data residency, local regulation, language).
5. **Score 0-100**: US proof 20%, EU white space 20%, structural EU gap 25%, build feasibility 15%, reachable buyers from Ireland 10%, EU investor appetite 10%. Append `{date, total, parts, sourced: true|false}` to the candidate's `scores`; mark any input you guessed as `sourced: false`. Bands: <60 low priority (retire only after 4 weeks below 60), 60-74 watch, 75+ validate.
6. **Update hypotheses.** For each thesis, append evidence for or against (with links), then add a conviction entry `{date, score 0-100, note}` that moves only because of new evidence. Add 1-3 new or sharpened theses with a claim, cheapest test and what would change your mind. Flag any category with 3+ rounds this week.
7. **Log the run** to `data/runs/YYYY-MM-DD.json` and add the date to `data/runs/index.json`. Log empty runs and blockers too.
8. **Commit and push to `main`.** Pages redeploys on push.
9. **Notify** (PushNotification) only for a 75+ candidate, a conviction move of 15+ points, a new 3+ round category, or a blocker that stopped the run. Otherwise stay silent.
10. **Digest** (5 lines): new rounds, top candidate, categories with 3+ rounds this week, biggest conviction change, blockers.

## Rules
- Never invent evidence, funding figures or competitors. Unknown means `null`, not a guess.
- Keep scores reproducible: store the parts, not just the total.
