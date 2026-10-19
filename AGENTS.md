# FIP coding-agent instructions

Read `docs/PROJECT_CONTEXT.md` and `docs/RESEARCH_SPEC.md` before feature work.

- Prioritize numerical accuracy, source provenance, reproducibility, data quality, and tests over polished AI prose.
- Never fabricate financial or KPI observations. Label observed, derived, estimated, illustrative, and unavailable values.
- Track company, segment, fiscal period, consolidation basis, units, metric definitions, source document/page, and observation version.
- Missing/not-disclosed is not zero. Check comparability before peer analysis; do not infer causation from correlation.
- Use deterministic Python/SQL for financial calculations. Use LLMs for business profiling, research planning, hypotheses, evidence evaluation, and synthesis.
- Seek disconfirming evidence and alternative explanations as well as supporting passages.
- Keep confidential deal memoranda, financials, personally identifiable data and derived deal-specific intelligence out of this public repository, shared databases, embeddings and logs. Do not send private materials to external APIs without authorization.
- Prefer small, reviewable commits with tests. Propose a plan before substantial implementation.
- Begin with backend data availability and deterministic analysis, rather than a complex agent framework or polished frontend.
