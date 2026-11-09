<h1 align="center">Hi, I'm Rihan Bagwan 👋</h1>
<h3 align="center">Data Engineer · DevOps & Linux · Python</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/rihanbagwan/"><img src="https://img.shields.io/badge/LinkedIn-rihanbagwan-0A66C2?logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:rihanbagwan98@gmail.com"><img src="https://img.shields.io/badge/Email-rihanbagwan98%40gmail.com-D14836?logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Location-Mumbai%2C%20India-555" alt="Mumbai, India">
  <img src="https://img.shields.io/badge/Open%20to-Data%20Engineering%20%26%20DevOps%20roles-2ea44f" alt="Open to work">
</p>

I'm a software engineer with **3+ years of experience**. For the last year I've focused on **data engineering**: I build
Python, PySpark and Airflow pipelines that load **15–20 GB a day into ClickHouse**, and I deploy and run them myself
on **RHEL Linux with Docker**.

### What I do

- 🛠️ **Build data pipelines.** I run 12+ ETL/ELT pipelines that pull from databases, REST APIs and CSV/XLSX/PDF files into ClickHouse (about 5M records a day).
- ✅ **Make data trustworthy.** Schema inference, validation and normalization cut rejected records by **~30%**.
- 🔁 **Make pipelines recover on their own.** Async ingestion with Celery, Redis and DuckDB, with retries and data recovery, cut failed loads by **~40%**.
- ⚙️ **Run what I build.** I handle Docker, RHEL administration, systemd/cron, Bash automation, CI/CD and log-driven troubleshooting. Fixing a memory bottleneck that caused job failures is part of the job.

### ⭐ Featured project

#### [batch-data-pipeline](https://github.com/the-iconic-rihan/batch-data-pipeline): Airflow → PySpark → Parquet → ClickHouse

An Airflow pipeline that ingests ~1M rows a day, validates and deduplicates them with PySpark, quarantines bad
rows with the reason they failed, and loads ClickHouse with an **atomic partition swap**, so re-runs never create
duplicates. You can start it with one command (`make up`), and GitHub Actions CI runs lint, PySpark unit tests,
a Docker build and a DAG integrity test on every push.

```mermaid
flowchart LR
    A[Raw CSV] --> B[Airflow DAG]
    B --> C[PySpark<br/>validate + dedupe]
    C --> D[Partitioned<br/>Parquet]
    C --> Q[Quarantine<br/>bad rows + reasons]
    D --> E[(ClickHouse<br/>atomic partition swap)]
```

### 🧰 Tech stack

**Data engineering**<br/>
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?logo=apachespark&logoColor=white)
![Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?logo=apacheairflow&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?logo=celery&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?logo=duckdb&logoColor=black)
![Parquet](https://img.shields.io/badge/Parquet-50ABF1?logo=apacheparquet&logoColor=white)

**Databases**<br/>
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?logo=clickhouse&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?logo=elasticsearch&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)

**DevOps & cloud**<br/>
![Linux](https://img.shields.io/badge/RHEL%20%2F%20Linux-EE0000?logo=redhat&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?logo=gnubash&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?logo=githubactions&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?logo=jenkins&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?logo=nginx&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonwebservices&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?logo=microsoftazure&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana&logoColor=white)

**Backend**<br/>
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white)

### 💼 Experience

| Role | Company | When | Focus |
|---|---|---|---|
| Software Development Engineer | Skillmine Technology Consulting | Nov 2025 – Present | ETL/ELT into ClickHouse, PySpark, Airflow, Celery, Docker on RHEL |
| Software Development Engineer | Reliance Jio Platforms | Jan 2024 – Nov 2025 | Data ingestion & sync, SQL tuning (−25% latency), Python/Bash automation on RHEL |
| Software Development Engineer | Dimensionless Technologies | Aug 2023 – Jan 2024 | GPT-3.5 automation, LLM data prep, real-time backends (WebSockets, asyncio) |

🎓 B.Tech in Computer Science, GH Raisoni College of Engineering and Management, Pune (2019–2023)<br/>
📄 Paper: *"GitHub Issue Manager System for Rank-Based Profile"*, ICET-23

---

<sub>Repositories from before 2023 are college and learning projects (web development, Python games). I've kept them as a record of where I started.</sub>
