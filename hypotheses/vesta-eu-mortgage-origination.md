# Hypothesis: Vesta -> EU/Irish mortgage-origination agents (AI Act-native)

Status: WATCH, top of band (74/100; 75 = validate). Drafted 2026-10-12. Press-reported figures, unverified.

## US proof
- Vesta: AI agents for mortgage origination (document review, data validation, underwriting decisions, condition clearing, closing review). $30M Series B, 8 Oct 2026, led by Conversion Capital. Existing lender customers Pennymac, New American Funding and nbkc invested; Citi Ventures and a16z participated. Total raised $85M.
- Reported: revenue up 12x in 12 months, lenders on the platform originate >$100B/yr, ~40% of platform tasks run through agents or automated workflows (task count, not auto-approved loans), market share <5%.
- Sources: https://techcrunch.com/2026/10/08/vesta-raises-30m-as-lenders-adopt-ai-agents/ , https://thenextweb.com/news/vesta-30m-mortgage-ai-agents-eu , https://www.housingwire.com/articles/vesta-raises-30-million-series-b-ai-loan-origination-system/

## EU competitors found
- No funded EU/UK AI-agent mortgage-origination startup found in 2026 searches (search was not exhaustive). Every 2026 AI mortgage round found was US: Vesta, Tidalwave ($22M A), Balerion ($6M seed), Copperlane ($4.1M seed), Elio ($5.1M pre-seed).
- Adjacent: Taktile (Berlin/NY), $110M Series C, June 2026, AI underwriting for business loans and claims. Business lending falls outside AI Act Annex III 5(b), which covers natural persons, so it faces a lighter regime and is not a direct competitor.
- Incumbents NOT yet checked: Hypoport/Europace, Finastra, Temenos, Stacc, Mortgage Brain, Twenty7tec, MQube (UK, partnered with InCol in Ireland, 2024). Check these before any build decision.

## Structural EU gap
1. EU AI Act: creditworthiness assessment of natural persons is high-risk (Annex III 5(b)): conformity assessment, registration, human oversight, logs, fundamental-rights impact assessment. Reported deferral to 2 Dec 2027 (Regulation (EU) 2026/1744, per TNW; conflicting source says Aug 2026 -> VERIFY in the Official Journal).
2. GDPR Art. 22 already restricts solely-automated decisions with significant effects such as a refused mortgage.
3. EBA Loan Origination and Monitoring Guidelines, DORA third-party risk, Mortgage Credit Directive: lenders need explainable, auditable decisions and vendors with EU hosting.
4. Document extraction and classification with human validation can stay outside high-risk, so a staged product is possible.
5. 27 national mortgage regimes, languages and document types make a US product hard to port.
Reading: US vendors face a real compliance and localisation barrier; an EU-native vendor that ships conformity-ready tooling turns that barrier into the moat. Risk: the barrier also raises the cost for the EU entrant.

## Score
| Factor | Weight | Score | Weighted |
|---|---|---|---|
| US proof | 20% | 90 | 18.0 |
| EU white space | 20% | 70 | 14.0 |
| Structural EU gap | 25% | 75 | 18.8 |
| Build feasibility | 15% | 60 | 9.0 |
| Reachable buyers from Ireland | 10% | 65 | 6.5 |
| EU investor appetite | 10% | 80 | 8.0 |
| **Total** | | | **74.3 -> 74 = WATCH (1 point under validate)** |

Weak points: Irish lender count is small (so reach has to extend to UK/NL/DACH), regulated-customer sales cycles are long, and the white-space score rests on a non-exhaustive search.

## Hypothesis
A document-first, EU-hosted mortgage origination agent (income and document verification, conditions, file QC) with built-in audit logs, human-in-the-loop sign-off and AI Act conformity tooling, sold to EU/UK lenders and brokers. Underwriting decisions come later, once conformity is in place. Start with Ireland as the reference market and the UK/NL as the first expansions.

## What moves it to VALIDATE (75+)
1. Check Europace, Finastra, Temenos, Stacc, MQube and Mortgage Brain for agentic features; confirm the white space (+5 on that factor would clear 75).
2. Verify the AI Act deferral date and Annex III scope for document-only workflows.
3. 8-10 conversations with Irish and UK lenders, brokers and credit unions on file-processing pain and vendor-approval process.
4. Confirm Vesta's metrics with HousingWire/TechCrunch primary text or a customer reference.

## Kill criteria
- An incumbent LOS vendor already ships agentic file processing with EU hosting.
- Lenders will only buy from vendors with existing bank references (no design-partner route).
- Per-lender integration cost makes sub-EUR 100k ACV deals unprofitable.
