# Ontology → KPI Linkage Demo

Live page: <https://yyyongnotageek.github.io/ontology-kpi-linkage/>

This is the deploy bundle. The source lives elsewhere; this repo only
contains the inlined `index.html` and the live data file.

## What it does

- Renders an ontology graph (5 master entities + 3 derived + new `agent_monthly`).
- Computes VNB over 500 agents × 6 months (Jan–Jun 2025) × 4 products.
- Provides a free-text Q&A panel: ask things like "How has VNB changed from Jan to Jun?",
  "What are the key factors?", "What if active ratio goes up by 5%?".
- Attribution is leave-one-out: each driver credited with the VNB change it caused,
  holding others at target. Residual is labeled as interaction effects.

## Data caveats

The v3 source data has only `CH001` (Agency) Agent Monthly + Product Mix rows.
CH002 (Banca) and CH003 (Brokerage) register 200 and 80 agents in the channel
sheet but have zero fact rows. The engine reports their APE/VNB as 0; the
attribution table flags `Channel Mix` as zero in v3.

## Build

This is a hand-inlined deploy. To rebuild from source, run
`scripts/build_deploy.py` in the source workspace.
