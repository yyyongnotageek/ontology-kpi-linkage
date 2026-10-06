# Ontology → KPI Linkage Demo

An interactive single-page demo that shows how operational KPIs propagate to
financial KPIs (VNB / APE / margin) through an insurance-actuarial ontology.

**Live:** https://yyyongnotageek.github.io/ontology-kpi-linkage/

## What it shows

- **5 ontology entities** — Product, VNB Summary, Distribution Channel, Agent,
  Product Mix — wired together with 5 relations.
- **3 derived entities** — Channel-Product VNB, Channel-Product APE,
  Overall VNB Margin — computed live from the operational inputs.
- **3 levers** — agency churn, bancassurance productivity, product-mix shift —
  each with a slider. Move them and watch VNB / margin update live.
- **Two-track KPI panel** — model view (live) vs realized reference (static,
  from the VNB Summary sheet).

## Files

- `index.html` — the standalone, self-contained bundle (vis-network inlined,
  no external dependencies, opens from `file://` as well).

## Source

See `second-brain/documents/ontology-kpi-linkage/` in the workspace where this
was authored. Ontology schema, xlsx → JSON conversion, build script, and
engine all live there.
