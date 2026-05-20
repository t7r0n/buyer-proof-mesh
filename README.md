# PreSales Proof Graph

A local proof-intelligence prototype that converts synthetic buyer requirements, demo evidence, objections, and product gaps into a reusable proof graph.

`presales-proof-graph` favors explicit fixtures, deterministic checks, and reviewable artifacts over hidden services or live data.

## Engineering target

PreSales Proof Graph: Buyer Requirements to Demo Evidence and Product Signals.

## How it works

- Synthetic opportunity, requirement, demo, objection, and feature-gap records.
- Proof coverage scoring with risk-ranked next-best actions.
- Evidence graph, decision report, and offline dashboard for stakeholder review.

## Run the system

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

## Evidence to inspect

- `outputs/dashboard.html`
- `outputs/decision_report.md`
- `outputs/evidence_graph.mmd`
- `outputs/risk_or_quality_report.csv`
- `outputs/benchmark.md`
- `outputs/demo_pack.md`

## Validation

```bash
uv run ruff check .
uv run pytest -q
uv run app verify
```

## Data boundary

`PreSales Proof Graph` is built for local reproduction: deterministic inputs enter the run, deterministic evidence comes out, and private data stays outside the repo.
