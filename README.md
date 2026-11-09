<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img src="assets/banner-light.svg" width="100%" alt="Rihan Bagwan: Data Engineer, DevOps & Linux, Python">
</picture>

<p align="center">
  <a href="https://the-iconic-rihan.github.io/Portfolio/"><img src="https://img.shields.io/badge/Portfolio-Visit_site-0f766e?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio website"></a>
  <a href="https://www.linkedin.com/in/rihanbagwan/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:rihanbagwan98@gmail.com"><img src="https://img.shields.io/badge/Email-Say_hello-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://the-iconic-rihan.github.io/Portfolio/assets/Rihan_Bagwan_Resume.pdf"><img src="https://img.shields.io/badge/Resume-PDF-24292F?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Resume PDF"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open_to-Data_Engineering_%26_DevOps_roles-2ea44f?style=flat-square" alt="Open to Data Engineering and DevOps roles">
</p>

## 👋 About me

I'm a software engineer with **3+ years of experience**. For the last year I've focused on **data engineering**:
Python, PySpark and Airflow pipelines that load **15–20 GB a day into ClickHouse**, which I also deploy and
run myself on **RHEL Linux with Docker**.

```yaml
name: Rihan Bagwan
role: Data Engineer · DevOps & Linux
location: Mumbai, India
now: Software Development Engineer @ Skillmine Technology Consulting
building:
  - ETL/ELT pipelines from databases, REST APIs and CSV/XLSX/PDF into ClickHouse
  - PySpark batch jobs orchestrated by Airflow (8 DAGs)
  - async ingestion with Celery, Redis and DuckDB
care_about: [data quality, idempotent re-runs, pipelines that recover on their own]
open_to: [Data Engineering, DevOps, Platform Engineering]
```

## 📈 Impact at a glance

<table align="center">
  <tr>
    <td align="center" width="160"><h3>15–20 GB</h3><sub>processed daily<br/>into ClickHouse</sub></td>
    <td align="center" width="160"><h3>12+</h3><sub>production<br/>ETL/ELT pipelines</sub></td>
    <td align="center" width="160"><h3>−40%</h3><sub>failed loads, via<br/>retries &amp; recovery</sub></td>
    <td align="center" width="160"><h3>−30%</h3><sub>rejected records,<br/>via validation</sub></td>
    <td align="center" width="160"><h3>−25%</h3><sub>SQL query<br/>latency</sub></td>
  </tr>
</table>

## ⭐ Featured project

<table>
  <tr>
    <td>
      <h3><a href="https://github.com/the-iconic-rihan/batch-data-pipeline">batch-data-pipeline</a></h3>
      <p>
        <a href="https://github.com/the-iconic-rihan/batch-data-pipeline/actions/workflows/ci.yml"><img src="https://github.com/the-iconic-rihan/batch-data-pipeline/actions/workflows/ci.yml/badge.svg" alt="CI status"></a>
      </p>
      <p>
        An Airflow pipeline that ingests <b>~1M rows a day</b>, validates and deduplicates them with <b>PySpark</b>,
        quarantines bad rows with the reason they failed, and loads <b>ClickHouse</b> through an
        <b>atomic partition swap</b>, so re-running a day never creates duplicates.
      </p>
      <ul>
        <li>✅ Data-quality gate: if more than 5% of a batch is bad, nothing is published</li>
        <li>🔁 Idempotent, incremental loads: one run = one day, safe to re-run or backfill</li>
        <li>📊 Every run's counts, errors and timings are recorded in a <code>pipeline_runs</code> table</li>
        <li>🐳 One-command setup with Docker Compose · ⚙️ GitHub Actions CI with PySpark tests</li>
      </ul>
      <p>
        <img src="assets/icons/airflow.svg" width="32" alt="Airflow">
        <img src="assets/icons/spark.svg" width="32" alt="PySpark">
        <img src="assets/icons/parquet.svg" width="32" alt="Parquet">
        <img src="assets/icons/clickhouse.svg" width="32" alt="ClickHouse">
        <img src="https://skillicons.dev/icons?i=postgres" width="32" alt="PostgreSQL">
        <img src="https://skillicons.dev/icons?i=docker" width="32" alt="Docker">
        <img src="https://skillicons.dev/icons?i=githubactions" width="32" alt="GitHub Actions">
      </p>
    </td>
  </tr>
</table>

```mermaid
flowchart LR
    A[Raw CSV] --> B[Airflow DAG]
    B --> C[PySpark<br/>validate + dedupe]
    C --> D[Partitioned<br/>Parquet]
    C --> Q[Quarantine<br/>bad rows + reasons]
    D --> E[(ClickHouse<br/>atomic partition swap)]
```

## 🧰 Tech stack

<table>
  <tr>
    <td width="170"><b>Languages</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=python" width="44" alt="Python">
      <img src="assets/icons/sql.svg" width="44" alt="SQL">
      <img src="https://skillicons.dev/icons?i=bash" width="44" alt="Bash"><br/>
      <sub>Python · SQL · Bash</sub>
    </td>
  </tr>
  <tr>
    <td><b>Data engineering</b></td>
    <td>
      <img src="assets/icons/spark.svg" width="44" alt="Apache Spark / PySpark">
      <img src="assets/icons/airflow.svg" width="44" alt="Apache Airflow">
      <img src="assets/icons/celery.svg" width="44" alt="Celery">
      <img src="assets/icons/pandas.svg" width="44" alt="Pandas">
      <img src="assets/icons/numpy.svg" width="44" alt="NumPy">
      <img src="assets/icons/duckdb.svg" width="44" alt="DuckDB">
      <img src="assets/icons/parquet.svg" width="44" alt="Apache Parquet"><br/>
      <sub>PySpark · Apache Airflow · Celery · Pandas · NumPy · DuckDB · Parquet · ETL/ELT · data validation · data modeling</sub>
    </td>
  </tr>
  <tr>
    <td><b>Databases</b></td>
    <td>
      <img src="assets/icons/clickhouse.svg" width="44" alt="ClickHouse">
      <img src="https://skillicons.dev/icons?i=postgres" width="44" alt="PostgreSQL">
      <img src="https://skillicons.dev/icons?i=mysql" width="44" alt="MySQL">
      <img src="https://skillicons.dev/icons?i=mongodb" width="44" alt="MongoDB">
      <img src="https://skillicons.dev/icons?i=elasticsearch" width="44" alt="Elasticsearch">
      <img src="https://skillicons.dev/icons?i=redis" width="44" alt="Redis"><br/>
      <sub>ClickHouse · PostgreSQL · MySQL · MongoDB · Elasticsearch · Redis</sub>
    </td>
  </tr>
  <tr>
    <td><b>DevOps &amp; CI/CD</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=docker" width="44" alt="Docker">
      <img src="https://skillicons.dev/icons?i=kubernetes" width="44" alt="Kubernetes">
      <img src="https://skillicons.dev/icons?i=githubactions" width="44" alt="GitHub Actions">
      <img src="https://skillicons.dev/icons?i=jenkins" width="44" alt="Jenkins">
      <img src="https://skillicons.dev/icons?i=gitlab" width="44" alt="GitLab CI">
      <img src="https://skillicons.dev/icons?i=git" width="44" alt="Git">
      <img src="https://skillicons.dev/icons?i=nginx" width="44" alt="Nginx">
      <img src="https://skillicons.dev/icons?i=grafana" width="44" alt="Grafana"><br/>
      <sub>Docker · Docker Compose · Kubernetes (basic) · GitHub Actions · Jenkins · GitLab CI · Git · Nginx · Grafana</sub>
    </td>
  </tr>
  <tr>
    <td><b>Cloud</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=aws" width="44" alt="AWS">
      <img src="https://skillicons.dev/icons?i=azure" width="44" alt="Azure"><br/>
      <sub>AWS · Azure</sub>
    </td>
  </tr>
  <tr>
    <td><b>Linux &amp; infra</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=redhat" width="44" alt="Red Hat Enterprise Linux">
      <img src="https://skillicons.dev/icons?i=linux" width="44" alt="Linux">
      <img src="https://skillicons.dev/icons?i=ubuntu" width="44" alt="Ubuntu"><br/>
      <sub>RHEL · Linux administration · Ubuntu · systemd · cron · yum/dnf · log analysis</sub>
    </td>
  </tr>
  <tr>
    <td><b>Backend &amp; automation</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=fastapi" width="44" alt="FastAPI">
      <img src="https://skillicons.dev/icons?i=django" width="44" alt="Django">
      <img src="https://skillicons.dev/icons?i=graphql" width="44" alt="GraphQL">
      <img src="https://skillicons.dev/icons?i=selenium" width="44" alt="Selenium">
      <img src="assets/icons/playwright.svg" width="44" alt="Playwright"><br/>
      <sub>FastAPI · Django · REST APIs · GraphQL · WebSockets · asyncio · Selenium · Playwright</sub>
    </td>
  </tr>
  <tr>
    <td><b>Also worked with</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=js" width="44" alt="JavaScript">
      <img src="https://skillicons.dev/icons?i=react" width="44" alt="React">
      <img src="https://skillicons.dev/icons?i=java" width="44" alt="Java">
      <img src="https://skillicons.dev/icons?i=html" width="44" alt="HTML">
      <img src="https://skillicons.dev/icons?i=css" width="44" alt="CSS">
      <img src="https://skillicons.dev/icons?i=vscode" width="44" alt="VS Code"><br/>
      <sub>JavaScript · React · Java · HTML · CSS · VS Code</sub>
    </td>
  </tr>
</table>

## 💼 Experience

| | Role | Focus |
|:--|:--|:--|
| **Nov 2025 – Present** | **Software Development Engineer** · Skillmine Technology Consulting | ETL/ELT into ClickHouse (15–20 GB/day), PySpark, Airflow, Celery, FastAPI, Docker on RHEL |
| **Jan 2024 – Nov 2025** | **Software Development Engineer** · Reliance Jio Platforms | Data ingestion &amp; sync, SQL tuning (−25% latency), Django, Python/Bash automation on RHEL |
| **Aug 2023 – Jan 2024** | **Software Development Engineer** · Dimensionless Technologies | GPT-3.5 automation (+35% efficiency), LLM data prep, real-time backends (WebSockets, asyncio) |

## 🎓 Education & publication

- **B.Tech in Computer Science**, GH Raisoni College of Engineering and Management, Pune (2019–2023)
- **Paper:** *"GitHub Issue Manager System for Rank-Based Profile"*, ICET-23

---

<p align="center">
  <b>Hiring for data engineering or DevOps?</b> I'd be glad to talk:
  <a href="mailto:rihanbagwan98@gmail.com">rihanbagwan98@gmail.com</a>
  <br/><br/>
  <sub>Repositories from before 2023 are college and learning projects. I've kept them as a record of where I started.</sub>
</p>
