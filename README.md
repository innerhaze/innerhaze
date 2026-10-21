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
The five-layer stack that ran in front of a client export: field invariants, schema
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
Preflight ahead of execution, punch-lists instead of mid-run questions, and the argument
for when an automated decision is justified at all: only when a downstream check bounds
the cost of getting it wrong.

**[paramo-thesis-summary](https://github.com/innerhaze/paramo-thesis-summary)**
Whether connectivity between Andean páramo fragments, which shifted through the
Pleistocene, can still be read in how Espeletiinae lineages diverged. It can: historical
connectivity explains divergence better than straight-line distance once patches are far
apart. Movement-cost surfaces from elevation and a paleoclimatic reconstruction, graph
metrics in Graphab across nineteen habitat configurations, a generalised dissimilarity
model in R. Links out to four repositories holding the code for each step.

---

## Where this comes from

Two years as the pre-sales data analyst at a location-data company. A prospective
customer would ask, through the sales team, whether our data could answer their
question: coverage of a brand in a market, a category across countries, where a
store's customers come from. I decided whether it could, produced the sample or the
analysis that answered it, and set the standard for whether it shipped.

That ran to roughly 126 sample intakes across more than a dozen markets in North
America, Europe, Asia, Latin America and the Middle East. After a year and a half of
doing the audits by hand I automated them, and ended up sole author of that pipeline.
It was one thread of the role, not the role.

The longest-running system I owned was the validation that runs before a client opens
an export: fifteen months, three codebases, a repository migration in between. I wrote three
of its five layers and extended the two that were already there.

---

## Before that

A biologist, Universidad de Antioquia. The thesis above is where the habits came
from: a number that looks plausible is not the same as a number that is right. It was
the last thing I did before the location-data work. The four repositories it links to
are the code for each step: the only substantial code here that is not a synthetic
reproduction.

Georeferencing for a university entomological collection in 2023, during the degree,
was my first paid work with spatial data.

---

## Tools

`Python` `SQL` `R` · `PostGIS` `Shapely` `GeoPandas` `H3` `alphashape` `OSMnx` `QGIS` `Graphab` · `pandas` `Polars` `NumPy` `SciPy` · `pytest` `Git`

---

## Contact

Medellín, Colombia · [sebasadmon@gmail.com](mailto:sebasadmon@gmail.com) · [LinkedIn](https://www.linkedin.com/in/sebastian-sanchez-cuartas)
