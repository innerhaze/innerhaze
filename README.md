# Sebastián Sánchez Cuartas

Hired as an early-career analyst at a location-data company to execute a sample-production process that already existed and to do quality control over geospatial deliverables. After a year of running the process by hand, I wrote two design documents proposing to automate it, and built what the documents proposed. I ended the role as the sole author of the pipeline that produces the company's client samples. The write-ups below are the pieces of that work that generalise.

### What I actually do

Validation layers that sit between a dataset and a client. Some I inherited and extended, some I designed. The ones I designed are value-level distribution profiling, record-level pattern scans, and a three-way congruence check across database, delivery export, and post-delivery scan. The ones I inherited and extended are the field-level invariants and the schema conformance checks.

Alongside that: an LLM-assisted review path that is only trusted on a write once a deterministic re-derivation agrees with it; mutation guards for a shared production table that cannot be migrated; and the piece most people don't publish about, codifying domain knowledge as executable configuration, so that rules learned from real incidents don't live in anyone's head.

### Where I come from

A biology degree with a thesis on landscape connectivity modelling in R: cost rasters, Graphab, a GDM analysis of evolutionary divergence in the Northern Andean páramos during the Pleistocene. That background is why I think about spatial data the way I do, polygons, distances and topology before dashboards.

### What is different about the way I work

Operational rules the team learned the hard way turn into executable registries with the originating incident attached. A specific chain whose records got mis-tagged a particular way becomes a line in a registry, not tribal knowledge in a channel. A container-plus-tenant merge collision becomes a pattern-scan rule, not a story told once at an onboarding. The registry carries its own history, and the next person who runs the pipeline reads it instead of being told.

---

### Selected work

**[mobility-catchment-analysis](https://github.com/innerhaze/mobility-catchment-analysis)** — Comparative study of grid-based and adaptive geometry for measuring real-world catchment areas from device location data. Visit detection by point-in-polygon, rule-based segmentation without ground truth, a hexagonal grid measured against convex and concave hulls, and a synthetic reproduction of the method.

**[data-validation-architecture](https://github.com/innerhaze/data-validation-architecture)** — The validation stack that sits in front of a client-facing data delivery, in the order it runs: field-level invariants, schema conformance, value-level distribution profiling, pattern scans at the record level, and a three-way congruence check against the database. Each layer only sees what the previous one accepted. A scope note delimits which layers are my design and which I inherited and extended.

**[llm-verification-patterns](https://github.com/innerhaze/llm-verification-patterns)** — Design notes on using a language model for per-record judgment without trusting any individual verdict. A three-layer contract, reviewer, deterministic verifier, sampling audit, that catches record-level mistakes, batch-level drift, and the long tail of wrong-at-high-confidence outputs that a threshold filter lets through.

**[safe-mutation-patterns](https://github.com/innerhaze/safe-mutation-patterns)** — Writing to a shared production table when you cannot add constraints or change the schema. A typed-reason mutation guard, deterministic-key idempotency without a migration, timeout classes picked by call site, and the discipline of documenting a service assumption that turned out to be wrong.

**[operator-driven-pipelines](https://github.com/innerhaze/operator-driven-pipelines)** — Design choices for a pipeline whose primary user is a human who knows the domain. Preflight that reports what manual actions are needed, execution that never asks a question mid-run, a punch-list at the end instead of modals, and the documentation suite a one-author system needs to survive a hand-off.

**[domain-rules-as-config](https://github.com/innerhaze/domain-rules-as-config)** — Design notes on where operational knowledge about a specific domain lives inside a data pipeline. Executable registries that run before the language model, rules that carry the originating incident with them, market context as structured input rather than prompt preamble, and an archetype pattern for routing records the automation is not qualified to resolve.

---

### Earlier work

Landscape connectivity modelling in R for a thesis on evolutionary divergence and historical connectivity in the Northern Andean páramos during the Pleistocene. Methodology, cost rasters, a Graphab–R integration, and the GDM analysis are in a set of smaller repositories, summarised in [paramo-thesis-summary](https://github.com/innerhaze/paramo-thesis-summary).

---

### Tools

`Python` `SQL` `R` · `PostGIS` `GeoPandas` `Shapely` `H3` `QGIS` `Graphab` · `pandas` `Polars` `NumPy` `SciPy` · `pytest` `Git`

---

Medellín, Colombia · sebasadmon@gmail.com · [LinkedIn](https://www.linkedin.com/in/sebastian-sanchez-cuartas)
