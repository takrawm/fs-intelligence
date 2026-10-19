# Research Specification v1.0 — public-safe PoC

## Research question
Under what conditions might integrating building demolition with industrial-waste collection, intermediate treatment and recycling improve operating profitability and return on invested capital, relative to specialist companies?

**Scope:** This repository holds only the reusable, public-safe specification. A separate permission-controlled deal workspace may apply the methodology to an actual acquisition candidate. No private information memorandum or deal-derived financial values are included here.

## Hypotheses and guardrails

| ID | Hypothesis | Primary method | Minimum caveat |
|---|---|---|---|
| H1 | In-house intermediate treatment can reduce total cost versus outsourcing | Matched treatment-route cost per unit, including transport, labor, depreciation, residues and overhead | Waste type, distance, capacity and accounting scope must match |
| H2 | Integrated service can increase win rate, retention or job gross margin | Compare integrated and standalone jobs, controlling for size, customer, prime-contract role, and complexity | Generally requires non-public job-level data |
| H3 | Higher utilization can dilute facility fixed costs and improve margin | Process-specific throughput versus **effective** capacity, fixed/variable cost per unit | Do not mix tons and m³ or double-count multistage throughput |
| H4 | Integration can improve ROIC when operating return outweighs capital investment | NOPAT margin × invested-capital turnover; CAPEX and FCF | Remove non-operating assets and harmonize capital/lease definitions |
| H5 | Outsourced demolition combined with owned treatment may offer favorable capital efficiency | Compare self-perform/outsource × treatment-own/outsource operating models | Control for business mix, region, company scale and disclosure limits |

## Financial data requirements
F-001 revenue; F-002 gross and operating profit; F-003 outsourcing/labor/material expenses; F-004 external waste treatment expense; F-005 fuel/repairs/depreciation; F-006 property, plant and equipment/capex; F-007 receivables/inventory/payables; F-008 interest-bearing and lease debt; F-009 non-operating assets/earnings normalization; F-010 job-/segment-level revenue and direct cost.

## Industry KPI requirements
K-001 jobs count; K-002 average contract value; K-003 prime-contractor ratio; K-004 in-house construction proportion; K-005 waste intake by type/facility; K-006 permitted and effective processing capacity by route; K-007 actual utilization; K-008 own-demolition waste treated in-house; K-009 waste treatment price by material/customer; K-010 recycling and residue ratios; K-011 fleet/haulage; K-012 site-manager productivity; K-013 bid win and repeat business; K-014 facility operating and contribution margins.

## Business-model attributes
B-001 sales mix; B-002 customer mix; B-003 building/job types; B-004 in-house vs outsourced construction; B-005 collection/intermediate/final disposal scope; B-006 facility ownership; B-007 waste types; B-008 vertical integration span; B-009 geography; B-010 prime/subcontractor role; B-011 permits; B-012 business scale.

Every observation must track entity/segment, period, units, consolidation and accounting basis, source/page, disclosed-vs-derived-vs-estimated classification, and version. Missing observations are NULL, never zero.

## Candidate peer groups
PG-01 integrated demolition/waste treatment; PG-02 demolition specialists; PG-03 intermediate treatment specialists; PG-04 facility-owning waste processors; PG-05 subcontract-heavy construction services. A listed company's segment may be a valid peer when the consolidated group is not.

## Execution protocol
1. Profile business activity and boundaries.
2. Discover peer candidates from publicly available sources.
3. Verify field availability, source access restrictions and comparison eligibility.
4. Compute quantitative contrasts and margin/ROIC decompositions in deterministic Python/SQL.
5. Form and revise hypotheses based on results; retrieve **supporting and disconfirming** evidence.
6. Distinguish observed fact, association, scenario simulation and causal estimate.
7. Report untestable claims and required internal diligence data.

## First milestone and acceptance gates
- Data availability matrix for 5–10 peers and F/K/B fields, with actual evidence of field availability.
- Every used figure traceable to source, unit, period, consolidation scope and definition.
- Every inclusion/exclusion of a peer explainable.
- H1–H5 each classified as testable, directionally assessable or insufficient-data.
- All numerical analyses reproducible from persisted data, parameters and versioned code.
- Do not claim causal effects from correlations or from simple differences in accounting metrics.

## Candidate sources to validate
EDINET and issuer filings, relevant construction-company disclosure and evaluation records, permitted industrial-waste facility/public-information systems, and Japanese governmental construction/environment statistics. Candidate listing is **not** verification of coverage, licensing or machine access.
