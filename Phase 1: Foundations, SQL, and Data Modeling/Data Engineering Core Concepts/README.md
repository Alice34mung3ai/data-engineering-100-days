# Data Engineering — Core Concepts

Personal study notes on core data engineering concepts, organized as a README for quick reference.

## Table of contents

- [What is Data Engineering?](#what-is-data-engineering)
- [Why Data Engineering Is Complex](#why-data-engineering-is-complex)
- [Data Maturity and Data Engineering](#data-maturity-and-data-engineering)
- [The Data Engineering Lifecycle](#the-data-engineering-lifecycle)
- [Storage Paradigms](#storage-paradigms)
- [Source Systems & Ingestion](#source-systems--ingestion)
- [Transformation](#transformation)
- [The Data Science Hierarchy of Needs](#the-data-science-hierarchy-of-needs)
- [Notes & References](#notes--references)

---

## What is Data Engineering?

Data engineering is the development, implementation, and maintenance of systems and processes that take in raw data and produce high-quality, consistent information that supports downstream use cases. Put another way: data engineering sits at the intersection of security, data management (DataOps), data architecture, orchestration, and software engineering.

## Why Data Engineering Is Complex

Data engineering must manage many moving parts while optimizing along several competing axes:

- Cost
- Agility
- Scalability
- Simplicity
- Reuse
- Interoperability

Modern tools abstract and simplify workflows compared with earlier generations, so today's data engineers focus less on building everything from scratch and more on selecting simple, cost-effective, best-of-breed services that deliver business value. A key responsibility is to create agile data architectures that can evolve with new technologies rather than becoming static and brittle.

## Data Maturity and Data Engineering

Data maturity describes an organization's progression toward higher data utilization. As maturity increases, the demands on the data engineering function and its architecture grow accordingly — requiring more robust processes, governance, and operational maturity.

## The Data Engineering Lifecycle

The lifecycle describes how data moves from raw sources to served data for analytics and ML. Common stages:

- Generation
- Ingestion
- Transformation
- Serving
- Storage

Storage underlies the entire lifecycle and isn't limited to a single stage.

### Undercurrents (cross-cutting concerns)

These concerns run across every lifecycle stage:

- Security
- Data management (DataOps)
- Data architecture
- Orchestration
- Software engineering

## Storage Paradigms

- Data Warehouse — Structured data only (e.g., tabular formats, CSV)
- Data Lake — Raw data, both structured and unstructured
- Lakehouse — Hybrid (combines structured and unstructured; e.g., Databricks, Snowflake lakehouse patterns)

Example tools commonly used by lifecycle stage:

- Ingestion — Cloud Dataflow (and other ingestion tools)
- Transformation — Dataprep, ETL/ELT frameworks
- Serving — Analytics platforms, ML features, Reverse ETL
- Storage — Snowflake, Databricks, other warehouses/lakehouses

## Source Systems & Ingestion

- Ingestion tooling is frequently written in Python and uses cloud services or streaming platforms.
- Ingestion patterns:
  - Batch — periodic, scheduled loads
  - Streaming — continuous, real-time ingestion (e.g., Kafka, Pub/Sub)

## Transformation

- OLTP (Online Transaction Processing) — optimized for fast transactional reads/writes (source systems).
- OLAP (Online Analytical Processing) — optimized for complex analytical queries (data warehouses).

## The Data Science Hierarchy of Needs

Based on Monica Rogati's pyramid, responsibilities are commonly split between data engineering (bottom layers) and data science (top layers):

1. Collect — instrumentation, logging, sensors, external data, and user-generated content (Data Engineering)
2. Store / Move / Process — reliable data flow and infrastructure (Data Engineering)
3. Aggregate / Label — cleaning, feature preparation, exploratory data analysis (Data Engineering)
4. Analytics — metrics, A/B testing, reporting (Data Science)
5. AI / ML — modeling and production ML systems (Data Science)

In practice, data scientists spend a large portion of their time in the bottom three layers gathering, cleaning, and processing data — work that data engineers enable and accelerate.

## Notes & References

These notes are based on foundational data engineering concepts and ideas aligned with "Fundamentals of Data Engineering" (Reis & Housley).

---

If you'd like, I can:
- Add a short example architecture diagram (ASCII or image link).
- Create a higher-level README at the Phase 1 directory.
- Split these notes into separate topic files (e.g., lifecycle.md, storage.md).
