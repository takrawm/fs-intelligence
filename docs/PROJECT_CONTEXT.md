# Financial Intelligence Platform — architecture context

## Purpose and initial scope
- Initial financial ingestion covers Japanese listed companies, public documents, major P/L, B/S and cash-flow accounts, with correction and update history.
- Initial audience is a small internal team.
- Financial Research offers reliable sourced financial/KPI information; Financial Intelligence uses it for peer selection, financial comparisons, hypotheses and research conclusions.
- A separate financial-modeling application owns company-specific forecasts and chosen assumptions. FIP provides top-down benchmark ranges and templates of bottom-up business drivers.

## Domain model
- Foundation: Company, Financial, Document.
- Extensions: Industry, BusinessModel, KPI/BusinessDriver, Benchmark, Evidence and ResearchExecution/Hypothesis.
- Business-model attributes and observations must be segment-aware and time-effective; businesses may span several industries.

## What differentiates the analysis
1. Select peers for a *research question*, rather than by industry-code match alone.
2. Track business similarity separately from financial disclosure completeness and comparison eligibility.
3. Quantitatively decompose margin and ROIC differences using deterministic calculations.
4. Connect observed financial differences to possible operational mechanisms.
5. Generate falsifiable hypotheses, find supporting and contradictory evidence, and report missing data and uncertainty.
6. Avoid weak regression claims when niche-industry sample sizes are too small.

## Suggested PoC stack (not yet an implementation decision)
- Python 3.12+, FastAPI/Pydantic, SQLAlchemy 2.x, Alembic.
- PostgreSQL and (when needed) pgvector/full-text search.
- pandas or Polars, SciPy/statsmodels, PyMuPDF, appropriate XBRL parsers.
- OpenAI API for semantic analysis; SQL/Python for numeric computation.
- pytest, Docker Compose and CI.
- React/TypeScript/shadcn/ui/Recharts after backend research workflows are validated.

## Provenance and repeatability
Persist research question/run, hypothesis, peer group and selection rationale, analysis execution with parameters/code version, source evidence including contradiction, conclusion, and immutable dataset snapshot reference.

## Next milestone
Perform a *Data Availability Assessment* for 5–10 candidate companies/segments across building demolition, construction-waste treatment, and construction subcontracting. Measure public-data coverage and comparison eligibility before automating deeper conclusions.

## Confidentiality
Public repository: only generic research methods, metadata schemas and non-sensitive examples. Case files and case-derived specifics remain in separately permissioned storage.
