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
  <br/>
  <img src="https://img.shields.io/badge/📍_India-Mumbai_·_Navi_Mumbai_·_Pune_·_Hyderabad_·_Bangalore-0f766e?style=flat-square" alt="India: Mumbai, Navi Mumbai, Pune, Hyderabad, Bangalore">
  <img src="https://img.shields.io/badge/🌍_Open_to_relocation-USA_·_UK_·_Europe_·_Singapore_·_Australia-1f6feb?style=flat-square" alt="Open to relocation: USA, UK, Europe, Singapore, Australia">
</p>

## 👋 About me

I'm a software engineer with **3+ years of experience**. For the last year I've focused on **data engineering**:
Python, PySpark and Airflow pipelines that load **15–20 GB a day into ClickHouse**, which I also deploy and
run myself on **Linux with Docker**.

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
preferred_locations:
  india: [Mumbai, Navi Mumbai, Pune, Hyderabad, Bangalore]
  relocation: [USA, UK, Europe, Singapore, Australia]
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
      <sub>Python · SQL · Bash · YAML</sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>Data engineering</b></td>
    <td>
      <img src="assets/icons/spark.svg" width="44" alt="Apache Spark">
      <img src="assets/icons/airflow.svg" width="44" alt="Apache Airflow">
      <img src="https://skillicons.dev/icons?i=kafka" width="44" alt="Apache Kafka">
      <img src="https://skillicons.dev/icons?i=rabbitmq" width="44" alt="RabbitMQ">
      <img src="assets/icons/celery.svg" width="44" alt="Celery">
      <img src="assets/icons/pandas.svg" width="44" alt="Pandas">
      <img src="assets/icons/numpy.svg" width="44" alt="NumPy">
      <img src="assets/icons/duckdb.svg" width="44" alt="DuckDB">
      <img src="assets/icons/parquet.svg" width="44" alt="Apache Parquet"><br/>
      <sub>PySpark · Apache Airflow · Apache Kafka · RabbitMQ · Celery · Pandas · NumPy · DuckDB · Parquet · dbt</sub><br/>
      <sub><i>Concepts: ETL / ELT · Batch &amp; streaming · CDC · Data modeling (star / snowflake) · Data quality · Incremental loads · Partitioning · Data lake / lakehouse</i></sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>Databases &amp; storage</b></td>
    <td>
      <img src="assets/icons/clickhouse.svg" width="44" alt="ClickHouse">
      <img src="https://skillicons.dev/icons?i=postgres" width="44" alt="PostgreSQL">
      <img src="https://skillicons.dev/icons?i=mysql" width="44" alt="MySQL">
      <img src="https://skillicons.dev/icons?i=mongodb" width="44" alt="MongoDB">
      <img src="https://skillicons.dev/icons?i=elasticsearch" width="44" alt="Elasticsearch">
      <img src="https://skillicons.dev/icons?i=redis" width="44" alt="Redis">
      <img src="https://skillicons.dev/icons?i=sqlite" width="44" alt="SQLite">
      <img src="https://skillicons.dev/icons?i=dynamodb" width="44" alt="DynamoDB"><br/>
      <sub>ClickHouse · PostgreSQL · MySQL · MongoDB · Elasticsearch · Redis · SQLite · DynamoDB</sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>Python backend</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=fastapi" width="44" alt="FastAPI">
      <img src="https://skillicons.dev/icons?i=django" width="44" alt="Django">
      <img src="https://skillicons.dev/icons?i=flask" width="44" alt="Flask">
      <img src="assets/icons/sqlalchemy.svg" width="44" alt="SQLAlchemy">
      <img src="assets/icons/pydantic.svg" width="44" alt="Pydantic">
      <img src="https://skillicons.dev/icons?i=graphql" width="44" alt="GraphQL">
      <img src="assets/icons/pytest.svg" width="44" alt="pytest">
      <img src="assets/icons/swagger.svg" width="44" alt="Swagger / OpenAPI"><br/>
      <sub>FastAPI · Django · Flask · SQLAlchemy · Pydantic · REST APIs · GraphQL · WebSockets · asyncio · pytest · Swagger / OpenAPI · Selenium · Playwright</sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>DevOps &amp; CI/CD</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=docker" width="44" alt="Docker">
      <img src="https://skillicons.dev/icons?i=kubernetes" width="44" alt="Kubernetes">
      <img src="https://skillicons.dev/icons?i=githubactions" width="44" alt="GitHub Actions">
      <img src="https://skillicons.dev/icons?i=jenkins" width="44" alt="Jenkins">
      <img src="https://skillicons.dev/icons?i=gitlab" width="44" alt="GitLab CI">
      <img src="https://skillicons.dev/icons?i=nginx" width="44" alt="Nginx"><br/>
      <sub>Docker · Docker Compose · Kubernetes · GitHub Actions · Jenkins · GitLab CI · Nginx</sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>Monitoring &amp; observability</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=prometheus" width="44" alt="Prometheus">
      <img src="https://skillicons.dev/icons?i=grafana" width="44" alt="Grafana">
      <img src="https://skillicons.dev/icons?i=elasticsearch" width="44" alt="Elasticsearch">
      <img src="assets/icons/kibana.svg" width="44" alt="Kibana"><br/>
      <sub>Prometheus · Grafana · ELK stack (Elasticsearch, Logstash, Kibana)</sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>AWS</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=aws" width="44" alt="Amazon Web Services"><br/>
      <sub>S3 · EC2 · Lambda · RDS</sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>Azure</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=azure" width="44" alt="Microsoft Azure"><br/>
      <sub>Blob Storage / ADLS Gen2 · Azure DevOps</sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>Linux &amp; shell tools</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=ubuntu" width="44" alt="Ubuntu">
      <img src="https://skillicons.dev/icons?i=linux" width="44" alt="Linux">
      <img src="https://skillicons.dev/icons?i=bash" width="44" alt="Bash">
      <img src="https://skillicons.dev/icons?i=vim" width="44" alt="Vim"><br/>
      <sub>Ubuntu · systemd · cron · SSH · rsync · grep / sed / awk · htop · apt · vim · tmux</sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>Developer tools</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=vscode" width="44" alt="VS Code">
      <img src="https://skillicons.dev/icons?i=pycharm" width="44" alt="PyCharm">
      <img src="https://skillicons.dev/icons?i=postman" width="44" alt="Postman">
      <img src="https://skillicons.dev/icons?i=git" width="44" alt="Git">
      <img src="https://skillicons.dev/icons?i=github" width="44" alt="GitHub">
      <img src="assets/icons/jira.svg" width="44" alt="Jira">
      <img src="assets/icons/jupyter.svg" width="44" alt="Jupyter"><br/>
      <sub>VS Code · PyCharm · Postman · Git · GitHub · Jira · Jupyter</sub>
    </td>
  </tr>
  <tr>
    <td width="170"><b>Engineering practices</b></td>
    <td>
      <sub>Microservices · REST API design · Event-driven architecture · Message queues · Caching · CI/CD · Infrastructure as Code · Containerization · OOP &amp; design patterns · System design · Unit &amp; integration testing · Code review · Agile / Scrum</sub>
    </td>
  </tr>
</table>

## 💼 Experience

| | Role | Focus |
|:--|:--|:--|
| **Nov 2025 – Present** | **Software Development Engineer** · Skillmine Technology Consulting | ETL/ELT into ClickHouse (15–20 GB/day), PySpark, Airflow, Celery, FastAPI, Docker on Linux |
| **Jan 2024 – Nov 2025** | **Software Development Engineer** · Reliance Jio Platforms | Data ingestion &amp; sync, SQL tuning (−25% latency), Django, Python/Bash automation on Linux |
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
