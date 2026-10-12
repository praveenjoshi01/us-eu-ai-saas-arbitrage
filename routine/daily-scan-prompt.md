# Daily US->EU AI SaaS arbitrage scan (v2, effective 2026-10-13)

Paste this into the scheduled routine's prompt. It replaces v1 (single 24h pass).

1. Search the last 24 hours of US AI funding news (Crunchbase News, Superpower Daily funding tracker, TechCrunch AI, US VC blogs). If the 24h window yields fewer than 3 qualifying rounds, widen to 7 days and say so.
2. Keep only US, application-layer AI SaaS rounds. For each: company, one-line product, stage, amount, lead fund, date, source link.
3. For each, check for European competitors (Dealroom, Crunchbase, LinkedIn, Sifted, EU-Startups, tech.eu) and note any structural EU gap (GDPR/AI Act, data residency, local regulation, language).
4. Score each 0-100: US proof 20%, EU white space 20%, structural EU gap 25%, build feasibility 15%, reachable buyers from Ireland 10%, EU investor appetite 10%. Under 60 drop, 60-74 watch, 75+ validate.
5. KEEP ITERATING until at least one candidate scores 75+ or you have exhausted these directions (stop after at most 6 rounds):
   a. Different verticals: insurance, mortgage/lending, legal, healthcare admin, accounting/AR, HR/recruiting, construction, logistics, real estate, cybersecurity/compliance.
   b. Different sources: trackers (aifunding.me, syncgtm, Crunchbase megadeals), VC blogs (a16z, Sequoia, Insight, Bessemer), press (HousingWire, Fintech Global, Axios Pro).
   c. Regulation-first: pick sectors where the AI Act (Annex III high-risk: credit, employment, insurance, education), GDPR Art. 22 or sector rules create an EU barrier, then look for US leaders there.
   d. Re-score near misses (70-74) after one more competitor check each (incumbents too, not just startups).
   e. Widen the window to 14 days if still empty.
6. Write each 60+ candidate as hypotheses/<company>-eu-<theme>.md in the repo (US proof, EU competitors, structural gap, score table, hypothesis, validation steps, kill criteria), and add a row to the first-pass doc https://claude.ai/code/artifact/2abf6397-dc78-4b57-9d9b-a2f8010d425b (if the Claude Docs connector is unavailable, say so and rely on the repo files). Commit and push to the session branch.
7. Verify before scoring: confirm round date, amount and lead against a primary or high-quality source; flag unverified claims. Never invent competitors; mark unchecked ones "not checked".
8. Notify (PushNotification) only when a candidate scores 75+, or a 60-74 candidate is new, or the run could not execute. Stay silent if nothing new.
9. Finish with a 5-line digest: new rounds found, top candidate and score, category with 3+ rounds this week, verification gaps, next step.
