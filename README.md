# Sebastián Sánchez Cuartas

**Geospatial data analyst.** I build the validation layers that decide whether location data is good enough to ship.

Biologist by training — landscape connectivity modelling in R — now working on point-of-interest data quality, audit pipelines, and LLM-assisted review with deterministic safety checks. Based in Medellín, working remotely in English.

---

### What I work on

**Data quality for geospatial deliverables.** Field-level and value-level validation, schema congruence checks, and pattern scans that catch ingestion defects before they reach a client: addresses that are really index strings, business names that are really unit labels, merge collisions between a building and its tenants.

**LLM pipelines that can be trusted on a write path.** Per-record model judgment is useful and unreliable in different measures. The pattern I keep returning to: let the model reason, then make a deterministic check re-derive the same conclusion from the underlying signals, and refuse the write when they disagree. Sample the agreements continuously so drift surfaces before it ships.

**Spatial analysis end to end.** Visit detection from mobile location data, catchment geometry, connectivity modelling, cost surfaces — from raw points through to something a non-technical reader can open in a browser and act on.

---

### Selected work

**[mobility-catchment-analysis](https://github.com/innerhaze/mobility-catchment-analysis)** — Comparative study of grid-based and adaptive geometry for measuring real-world catchment areas from device location data. Visit detection by point-in-polygon, rule-based segmentation without ground truth, a hexagonal grid measured against convex and concave hulls, and a synthetic reproduction of the method.

**[llm-verification-patterns](https://github.com/innerhaze/llm-verification-patterns)** — Design notes on using a language model for per-record judgment without trusting any individual verdict. A three-layer contract — reviewer, deterministic verifier, sampling audit — that catches record-level mistakes, batch-level drift, and the long tail of wrong-at-high-confidence outputs that a threshold filter lets through.

**[data-validation-architecture](https://github.com/innerhaze/data-validation-architecture)** — The validation stack that sits in front of a client-facing data delivery, in the order it runs: field-level invariants, schema conformance, value-level distribution profiling, pattern scans at the record level, and a three-way congruence check against the database. Each layer only sees what the previous one accepted.

**[safe-mutation-patterns](https://github.com/innerhaze/safe-mutation-patterns)** — Writing to a shared production table when you cannot add constraints or change the schema. A typed-reason mutation guard, deterministic-key idempotency without a migration, timeout classes picked by call site, and the discipline of documenting a service assumption that turned out to be wrong.

**[operator-driven-pipelines](https://github.com/innerhaze/operator-driven-pipelines)** — Design choices for a pipeline whose primary user is a human who knows the domain. Preflight that reports what manual actions are needed, execution that never asks a question mid-run, a punch-list at the end instead of modals, and the documentation suite a one-author system needs to survive a hand-off.

---

### Behind the write-ups

The write-ups above are drawn from two years of in-house work at a location-data company whose code is not mine to publish. The main things built there, described generically:

- **An operator-driven audit pipeline** that validates a brand's data coverage against external store counts, auto-corrects safe metadata gaps where it can, triggers duplicate and chain-assignment reports, and populates a client-deliverable sample. Twenty numbered steps and a core layer of single-purpose modules. The three-layer verification contract from `llm-verification-patterns` is the pipeline's highest-priority rule.
- **Post-export validation layers** running in front of every client deliverable, in the order described in `data-validation-architecture`: field invariants, schema conformance, value profiling, pattern scan, three-way congruence.
- **Internal tooling** to support both, including an MCP server the team uses from Claude Code and Claude Desktop as a front end for the operational tool catalogue.

That code is private. The write-ups above are the part of the method that generalises and that I can share.

---

### Earlier work

Landscape connectivity modelling in R for a thesis on evolutionary divergence and historical connectivity in the Northern Andean páramos during the Pleistocene. Methodology, cost rasters, a Graphab–R integration, and the GDM analysis are in a set of smaller repositories, summarised in [paramo-thesis-summary](https://github.com/innerhaze/paramo-thesis-summary).

---

### Tools

`Python` `SQL` `R` · `PostGIS` `GeoPandas` `Shapely` `H3` `QGIS` `Graphab` · `pandas` `Polars` `NumPy` `SciPy` · `pytest` `Git`

---

📍 Medellín, Colombia · 📧 sebasadmon@gmail.com · [LinkedIn](https://www.linkedin.com/in/sebastian-sanchez-cuartas)
