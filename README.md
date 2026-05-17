# PreSales Proof Graph

A local proof-intelligence prototype that converts synthetic buyer requirements, demo evidence, objections, and product gaps into a reusable proof graph.

## Features

- Synthetic opportunity, requirement, demo, objection, and feature-gap records.
- Proof coverage scoring with risk-ranked next-best actions.
- Evidence graph, decision report, and offline dashboard for stakeholder review.

## Run Locally

```bash
uv sync
uv run app init-demo
uv run app ingest fixtures/
uv run app analyze
uv run app verify
uv run app dashboard
uv run app benchmark
uv run app export-demo-pack
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/dashboard.html`
- `outputs/decision_report.md`
- `outputs/evidence_graph.mmd`
- `outputs/risk_or_quality_report.csv`
- `outputs/benchmark.md`
- `outputs/demo_pack.md`

## Data Policy

This project runs fully locally on deterministic synthetic fixtures. It does not require external APIs, credentials, private datasets, network access, or production systems.
