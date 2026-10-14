<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&duration=2800&pause=800&color=2F81F7&center=true&vCenter=true&width=860&lines=Data+Engineer;Spark+%7C+Databricks+%7C+Delta+Lake;Kafka+%7C+Airflow+%7C+Snowflake;RAG%2C+vector+search%2C+LLM+pipelines;Measuring+what+the+tooling+cannot+report." alt="Data Engineer. Spark, Databricks, Delta Lake. Kafka, Airflow, Snowflake. RAG, vector search, LLM pipelines. Measuring what the tooling cannot report." />

<br/>

<img src="https://img.shields.io/badge/experience-5%2B%20years-2F81F7?style=flat-square" alt="5 plus years" />
<img src="https://img.shields.io/badge/repositories-7-2F81F7?style=flat-square" alt="7 repositories" />
<img src="https://img.shields.io/badge/tests-1%2C845-3FB950?style=flat-square" alt="1845 tests" />
<img src="https://img.shields.io/badge/coverage-100%25%20line%20and%20branch-3FB950?style=flat-square" alt="100 percent line and branch coverage" />
<img src="https://img.shields.io/badge/decision%20records-31-8957E5?style=flat-square" alt="31 architecture decision records" />

</div>

---

## 👋 hey, I'm Sruthi

Data engineer, five years of it. Healthcare data platforms at Fortis in India,
a master's in data engineering at the University of North Texas, and lakehouse
and GenAI work at Meta since 2024. Day to day that is Spark and Databricks on
Delta Lake, Kafka and Airflow moving the data, and more recently RAG pipelines
and vector search over enterprise documents.

```
Aug 2019 ──────────── Dec 2022     · · · · · ·     Jun 2024 ──────────────▶
Fortis Healthcare, India           MS Data Eng     Meta, USA
ETL on AWS Glue and Redshift.      UNT, Denton     Databricks lakehouse,
Hadoop, Kafka, Kinesis, Airflow,                   Delta Lake, structured
DynamoDB, SSIS, Informatica.                       streaming, OpenAI and
                                                   LangChain pipelines, RAG.
```

The shape of that move is from making data arrive to making data defensible.
In India the hard part was volume and heterogeneity. At Meta the hard part is
that the things we build are now feeding models, and a model will happily learn
from a pipeline that is quietly wrong. The repositories below are what I do
with that worry.

---

## 🧭 what I publish here, and why it is not more pipelines

> Most of what I build at work is a pipeline. Most of what I publish here is a
> measurement of something a pipeline structurally cannot report about itself.
> A query plan cannot report the per-file cost that dominates a scan. A log
> cannot record what a streaming job decided to forget. recall@k cannot tell a
> retrieval failure from a chunking failure. Each repository takes one of those
> gaps, builds the smallest honest thing that measures it, and leads with the
> number that is least flattering to the design.

---

## 📊 seven repositories, 1,845 tests

| repository | what it measures that the usual tool cannot | the number it leads with | tests |
| --- | --- | --- | --- |
| [stream-replay-divergence](https://github.com/Sruthi0510-data/stream-replay-divergence) | what a replay of a stateful streaming job cannot reproduce | **62.0%** of output rows survive reprocessing, and 205 sessions become 12 | 402 |
| [merge-order-sensitivity](https://github.com/Sruthi0510-data/merge-order-sensitivity) | which CDC merge outcomes the delivery model can actually reach | **8.0%** of keys are order dependent, and a permutation harness finds 18 of the 32 | 359 |
| [rag-failure-attribution](https://github.com/Sruthi0510-data/rag-failure-attribution) | whether a RAG miss belongs to the retriever or to the chunker | **81.1%** of the misses are severance, not retrieval | 276 |
| [dq-detectability-audit](https://github.com/Sruthi0510-data/dq-detectability-audit) | what a data quality suite can detect at the sample size it runs on | **15 of 40** rules cannot fail, and 13 of those block a release | 251 |
| [llm-label-churn](https://github.com/Sruthi0510-data/llm-label-churn) | what a prompt change did, which an accuracy delta cannot say | **2,248** labels moved for a net gain of 13 items | 210 |
| [sql-dialect-drift](https://github.com/Sruthi0510-data/sql-dialect-drift) | whether transpiled SQL means the same thing, not just parses | **10 of 11** ordinary queries mean different things on six warehouses | 191 |
| [small-files-read-amplification](https://github.com/Sruthi0510-data/small-files-read-amplification) | the per-file cost a query plan is structurally blind to | **86.2%** of the scan is the half no plan reports | 156 |

Every number above is produced by code that ran, written into `docs/metrics.json`,
and matched against the sentence quoting it by a checker that fails the build
when the two disagree.

---

## 🛠 what I work with

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD4?style=for-the-badge&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)

![Apache Airflow](https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)

---

## 📐 depth, with the yardstick stated

The test is whether I could debug it in production at three in the morning, or
whether I have only ever shipped with it. Badges say nothing about that, so
here is the honest version.

| | depth | level, and where it came from |
| --- | --- | --- |
| **Python** | `█████████░` | **I debug this at 3am.** Every pipeline I have written for five years, and all 1,845 tests above |
| **SQL** | `█████████░` | **I debug this at 3am.** Redshift, Snowflake, BigQuery, Postgres, Oracle. `sql-dialect-drift` models six engines as the decisions they differ on |
| **Spark and PySpark** | `████████░░` | **Shipped and tuned it.** Distributed workloads at Meta, tuned by partitioning, caching and reading execution plans |
| **Databricks and Delta Lake** | `████████░░` | **Shipped and tuned it.** Lakehouse pipelines at Meta. `merge-order-sensitivity` audits what a Delta merge can actually produce |
| **Kafka and streaming** | `███████░░░` | **Shipped it.** Ingestion at Fortis, Structured Streaming at Meta. `stream-replay-divergence` is the measurement that came out of it |
| **Airflow and orchestration** | `███████░░░` | **Shipped it.** Production DAGs in both roles, plus Glue, Step Functions and SSIS before that |
| **AWS** | `███████░░░` | **Shipped it.** S3, Glue, Redshift, Lambda, EMR, Kinesis. Certified Data Engineer Associate |
| **RAG, embeddings, vector search** | `██████░░░░` | **Building with it.** OpenAI and LangChain pipelines at Meta. `rag-failure-attribution` is me trying to make the evaluation honest |
| **Statistics applied to data quality** | `██████░░░░` | **Building with it.** `dq-detectability-audit` and `llm-label-churn`: power, paired tests, design effects |

---

## 🧪 how all seven are built

- **The uncomfortable number is the headline.** The figure at the top of each
  README is the one that makes the design look worst, not the one that sells it.
- **Nothing is published that a machine did not re-measure.** `tools/collect_metrics.py`
  re-runs every experiment, `tools/check_numbers.py` fails the build when a
  document quotes a figure the code no longer produces, and CI regenerates the
  tables and diagrams and fails if a committed file changes.
- **Offline and deterministic.** No credentials, no cloud account, no network
  call at runtime. `pip install -e ".[dev]" && make verify` on a laptop with
  the wifi off, on Python 3.11, 3.12 and 3.13.
- **The bugs the measurement found are in the README.** Each repository has a
  section for the times the instrument was wrong, including a build that could
  not regenerate itself and a figure that moved between runs because of hash
  randomisation.

---

## 🎓 credentials

![AWS Certified Data Engineer Associate](https://img.shields.io/badge/AWS%20Certified-Data%20Engineer%20Associate-FF9900?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![MS Data Engineering](https://img.shields.io/badge/MS%20Data%20Engineering-University%20of%20North%20Texas-00853E?style=for-the-badge&logoColor=white)

---

## 📬 connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sruthisusarla/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:laxmisusarla@mycvcareer.com)

<div align="center">

<br/>

*"Testing shows the presence, not the absence of bugs."*
<br/>
Edsger W. Dijkstra

</div>
