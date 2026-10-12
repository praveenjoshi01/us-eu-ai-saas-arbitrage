# Hypothesis: Stuut -> EU order-to-cash agent (Ireland-based)

Status: WATCH (69/100). Drafted 2026-10-12. Source figures are press-reported and company-claimed, not independently verified.

## US proof
- Stuut: AI agents for order-to-cash (collections, cash application, disputes, deductions). Series B $52.5M, 7 Oct 2026, led by Insight Partners, with a16z and M12. Total raised $93M; Series A was $29.5M (a16z, Nov 2025), a 1.8x step-up.
- Claimed: DSO -47%, 81.7% of outbound collections touches run without a human, 95% auto cash-match. No methodology disclosed.
- Sources: https://www.axios.com/pro/fintech-deals/2026/10/07/stuut-52-5-million-series-b-insight-partners , https://techfundingnews.com/stuut-raises-52-5m-from-insight-partners-and-a16z-to-let-ai-agents-chase-enterprises-unpaid-invoices/

## EU competitors found
- Cleavr (Paris): EUR 8M seed, 6 Oct 2026, led by Varsity (EUR 1M pre-seed in Mar 2026). Closest direct copy. https://tech.eu/2026/10/06/cleavr-bags-eur8m-to-scale-ai-powered-invoice-collection-across-europe/
- Paraglide (Malmo) EUR 4.2M, Donnerstag.ai (Frankfurt) EUR 4.3M, sunbay.io (Warsaw) EUR 0.55M, Mimo EUR 7.7M (adjacent).
- Not checked (search returned nothing): Upflow, Billie, Kolleno, Peakflo, Tesorio, HighRadius EU presence. Check on Dealroom before any build decision.

## Structural EU gap (the actual arbitrage)
1. Multilingual, per-country collections: dunning tone, legal notice formats and statutory interest rules differ by member state.
2. E-invoicing mandates (Peppol, France 2026 rollout, German B2B, ViDA): structured-invoice-native agents beat PDF-parsing US tools.
3. GDPR: debtor contact data and automated decisions (Art. 22) push buyers toward EU data residency. AI Act exposure is likely limited-risk, but needs a legal check.
4. Late-payment pressure: EU late-payment rules and proposals raise the cost of slow collection.
Caveat: the gap is real but narrow, and Cleavr is already aiming at it.

## Score
| Factor | Weight | Score | Weighted |
|---|---|---|---|
| US proof | 20% | 85 | 17.0 |
| EU white space | 20% | 45 | 9.0 |
| Structural EU gap | 25% | 65 | 16.3 |
| Build feasibility | 15% | 70 | 10.5 |
| Reachable buyers from Ireland | 10% | 85 | 8.5 |
| EU investor appetite | 10% | 75 | 7.5 |
| **Total** | | | **68.8 -> 69 = WATCH** |

Rationale for the lows: white space is thin because at least four funded EU entrants exist. Feasibility is held back by ERP integration depth (SAP, NetSuite, Dynamics), not by the LLM layer.

## Hypothesis
A horizontal Stuut clone loses to Cleavr and to Stuut itself expanding. A wedge could work: an EU-resident, e-invoicing-native, multilingual collections and cash-application agent sold to Dublin shared-service centres of US multinationals and to Irish/EU mid-market, where one AR team chases debtors across 5-10 countries and languages.

## Validation (to move WATCH -> VALIDATE, need 75+)
1. 10 interviews with AR/finance-ops leads at Dublin SSCs: pain on multi-country dunning, willingness to pay, current tools.
2. Confirm which of Upflow/Billie/Kolleno/HighRadius already cover multilingual plus e-invoicing; document gaps.
3. Legal read: GDPR Art. 22 and AI Act classification for automated debtor communications.
4. Verify Stuut metrics via customer references or case studies.

## Kill criteria
- Dublin SSC buyers already standardised on HighRadius/Billtrust with no appetite to switch.
- Cleavr or Upflow ships SAP-grade integrations and multilingual compliance within 6 months.
- ERP integration cost per customer exceeds ~EUR 30k, which breaks mid-market unit economics.
