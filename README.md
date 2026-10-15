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

**[Mobility catchment analysis](https://github.com/innerhaze/mobility-catchment-analysis)** — Comparative study of grid-based and adaptive geometry for measuring real-world catchment areas from device location data. Visit detection by point-in-polygon, rule-based segmentation without ground truth, and a hexagonal grid measured against convex and concave hulls. Write-up covers method, validation reasoning, and what I would do differently.

**Connectivity modelling in Andean páramos** — My thesis work and the R tooling around it: generalised dissimilarity modelling of evolutionary divergence against historical connectivity, DEM reclassification from paleoclimatic data, and an R–Java integration that automates Graphab cost-surface processing across runs.

→ Repositories below. The connectivity work is from 2024; the data-quality and pipeline work from 2025–2026 lives in private repositories, so what I can show publicly is the method rather than the code.

---

### Tools

`Python` `SQL` `R` · `PostGIS` `GeoPandas` `Shapely` `H3` `QGIS` `Graphab` · `pandas` `Polars` `NumPy` `SciPy` · `pytest` `Git`

---

📍 Medellín, Colombia · 📧 sebasadmon@gmail.com · [LinkedIn](https://www.linkedin.com/in/sebastian-sanchez-cuartas)
