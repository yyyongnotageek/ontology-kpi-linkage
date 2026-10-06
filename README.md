# Ontology → KPI Linkage Demo

An interactive single-page demo that shows how operational KPIs propagate to
financial KPIs (VNB / APE / margin) through an insurance-actuarial ontology,
**with a third panel that drills into EV bridge variance and VNB attribution**.

**Live:** https://yyyongnotageek.github.io/ontology-kpi-linkage/

## What it shows

### Panel 1 — Ontology graph (top)
- **5 ontology entities** — Product, VNB Summary, Distribution Channel, Agent,
  Product Mix — wired together with 5 relations.
- **3 derived entities** — Channel-Product VNB, Channel-Product APE,
  Overall VNB Margin — computed live from the operational inputs.
- **3 levers** — agency churn, bancassurance productivity, product-mix shift —
  each with a slider. Move them and watch VNB / margin update live.
- **Two-track KPI panel** — model view (live) vs realized reference (static,
  from the VNB Summary sheet).

### Panel 2 — EV Bridge & VNB Attribution (bottom, NEW)
- **EV P&L Bridge waterfall** — opens at $100m, walks through VNB and 7 variance
  components, closes at $115m.
- **VNB radial network** — VNB center, 5 primary drivers (Assumption Change
  Impact, Active Agent Count, Business Mix, Agent Activity Ratio, Agent
  Average Case Size), each with 2–4 sub-drivers (Persistency, Mortality, Lapse,
  Expenses, Commissions, etc.).
- **Attribution table** — Driver | $-impact | share-of-movement %.

The 3 levers drive both panels:
- **Churn** → Active Agent Count driver
- **Productivity** → Agent Activity Ratio + Agent Average Case Size drivers
- **Mix** → Business Mix + Assumption Change Impact drivers

## Files

- `index.html` — the standalone, self-contained bundle (vis-network inlined,
  no external dependencies, opens from `file://` as well).

## Source

See `second-brain/documents/ontology-kpi-linkage/` in the workspace where this
was authored. Ontology schema, xlsx → JSON conversion, build script, engine,
SVG renderers all live there.
