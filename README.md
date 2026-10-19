# Sebastián Sánchez Cuartas

I work on the quality side of commercial location data: deciding whether a dataset
can answer the question someone is asking, and building the checks that make that
answer hold.

Most of what I build at work is private. What is here is the method, rewritten
from scratch against synthetic data so it can be read and run.

---

## What's here

**[mobility-catchment-analysis](https://github.com/innerhaze/mobility-catchment-analysis)**
Where a store's customers come from, and how to tell staff from customers in device
data with nothing labelled. Compares a fixed H3 grid against convex and concave hulls
fitted to the observed points, and explains why the grid imposes a shape the data does
not have. Runnable reproduction with synthetic pings, three figures and an interactive
map.

**[data-validation-architecture](https://github.com/innerhaze/data-validation-architecture)**
The five-layer stack that ran in front of every client export: field invariants, schema
conformance, value-level profiling, record-level pattern scans, three-way database to
export congruence. Written in the order the layers run, with the reasoning for the
order and the defect classes each one caught.

**[llm-verification-patterns](https://github.com/innerhaze/llm-verification-patterns)**
When a model's verdict can be trusted enough to write to production. A reviewer, an
independent deterministic check that re-derives the decision from the numbers, and a
sampling audit that halts the batch on disagreement. Includes why a confidence
threshold does not solve this, and when to replace the model with a static rule.

**[domain-rules-as-config](https://github.com/innerhaze/domain-rules-as-config)**
Expert judgment written down as executable configuration instead of living in one
person's head. Rule registries that carry their own rationale, market context as
structured input rather than prose in a prompt, and the cases where the system should
stop and ask rather than decide.

**[safe-mutation-patterns](https://github.com/innerhaze/safe-mutation-patterns)**
Writing to a shared production table you do not own and cannot migrate. Typed-reason
guards, idempotency through a deterministic hash, per-query-class timeouts, and what
to do when a service does not behave the way the team assumes.

**[operator-driven-pipelines](https://github.com/innerhaze/operator-driven-pipelines)**
Designing a pipeline for a domain expert to run rather than an engineer to maintain.
Preflight ahead of execution, punch-lists instead of mid-run prompts, failure modes
that a non-engineer can act on.

**[paramo-thesis-summary](https://github.com/innerhaze/paramo-thesis-summary)**
Landscape connectivity modelling in Andean páramo: movement-cost surfaces from a
digital elevation model and a paleoclimatic reconstruction, graph metrics across
nineteen habitat configurations, results related to genetic divergence with a
generalised dissimilarity model.

---

## Where this comes from

Two years as the pre-sales data analyst at a location-data company. A prospective
customer would ask, through the sales team, whether our data could answer their
question: coverage of a brand in a market, a category across countries, where a
store's customers come from. I decided whether it could, produced the sample or the
analysis that answered it, and set the standard for whether it shipped.

That ran to about 126 sample deliveries across more than a dozen markets in North
America, Europe, Asia, Latin America and the Middle East. After eighteen months of
doing the audits by hand I automated them, and ended up sole author of the pipeline
that replaced the manual process — 208 commits, around 1,400 tests.

The longest thread was the validation that runs on every export before a client opens
it: fifteen months, three codebases, a repository migration in between. I wrote three
of its five layers and extended the two that were already there.

---

## Before that

A biologist. The thesis above is where the habits came from: a number that looks
plausible is not the same as a number that is right.

Georeferencing for a university entomological collection, 2023, which is where spatial
data stopped being a thesis method and became the work. Five years as a teaching
assistant in botany and animal biology. A year reviewing legal documentation in English
for a US non-profit, which is why I have been working in English since 2021.

---

## Tools

`Python` `SQL` `R` · `PostGIS` `Shapely` `GeoPandas` `H3` `alphashape` `OSMnx` `QGIS` `Graphab` · `pandas` `Polars` `NumPy` `SciPy` · `pytest` `Git`

---

## Contact

Medellín, Colombia · [sebasadmon@gmail.com](mailto:sebasadmon@gmail.com) · [LinkedIn](https://www.linkedin.com/in/sebastian-sanchez-cuartas)
