<h1 align="left"> Hi, I'm Sumit Vishwakarma</h1>

<p align="left">
  <b>Aspiring AI Data Engineer</b> · Python · SQL · PySpark<br/>
  Azure · Databricks · Microsoft Fabric · RAG · LangChain · LangGraph
</p>

<p align="left">
  <a href="https://linkedin.com/in/svwxyz"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:svisemployed@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" /></a>
  <img src="https://img.shields.io/badge/Open_to-Data_Engineering_roles-2ea44f?style=flat" />
</p>

---

## 🧭 About Me

I'm a BCA student at **MERI, New Delhi** (graduating 2027) building towards a career as an **AI Data Engineer**: the person who builds the data foundations that make AI applications reliable. I like turning raw, messy data into clean, analytics-ready tables, and now into the pipelines that feed **LLM and RAG systems**.

- 🔭 Currently building: lakehouse and warehouse projects on **Azure** and **Microsoft Fabric**
- 🤖 Built a **RAG assistant** with LangChain, OpenAI and Chroma, and now learning **LangGraph** agent workflows
- 🌱 Currently deepening: **Delta Lake**, **Airflow** orchestration, dimensional modeling
- 🏆 Won **1st place** in a college SQL query optimization contest
- 📫 Reach me at **svisemployed@gmail.com**

---

## 🛠️ Tech Stack

### 🧑‍💻 Languages & Analytics
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white" />
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white" />
</p>

### ☁️ Data Engineering & Cloud
<p>
  <img src="https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoftazure&logoColor=white" />
  <img src="https://img.shields.io/badge/Azure_Data_Factory-0078D4?style=flat&logoColor=white" />
  <img src="https://img.shields.io/badge/Azure_Data_Lake-0078D4?style=flat&logoColor=white" />
  <img src="https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white" />
  <img src="https://img.shields.io/badge/Delta_Lake-00ADD4?style=flat&logo=delta&logoColor=white" />
  <img src="https://img.shields.io/badge/Microsoft_Fabric-6A5ACD?style=flat&logoColor=white" />
  <img src="https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white" />
</p>

### 🤖 AI & LLMs
<p>
  <img src="https://img.shields.io/badge/LLMs-412991?style=flat&logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/RAG-FF6F00?style=flat&logoColor=white" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white" />
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langgraph&logoColor=white" />
</p>

### 📊 BI & Visualization
<p>
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Tableau-E97627?style=flat&logo=tableau&logoColor=white" />
  <img src="https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white" />
</p>

### 🏗️ Concepts
`ETL / ELT` · `Star Schema` · `Fact & Dimension Modeling` · `Data Warehousing` · `Medallion Architecture` · `Parquet` · `Query Optimization` · `Retrieval-Augmented Generation (RAG)` · `LLM Agent Workflows`

---

## 🚀 Featured Projects

### 🤖 DataForge RAG: AI Assistant over *Fundamentals of Data Engineering*
`Python` · `LangChain` · `OpenAI LLM & Embeddings` · `Chroma` · *Phase 1 completed Aug 2026*

- Built a **RAG pipeline** that answers questions from a large data engineering book (PDF) using only retrieved context
- Loaded the PDF with `PyPDFLoader`, split it with `RecursiveCharacterTextSplitter` (with chunk overlap) and embedded the chunks with **OpenAI Embeddings**
- Stored vectors in **Chroma**, retrieved the most relevant chunks via semantic similarity search, injected them into a prompt template and generated grounded answers with an **OpenAI LLM**

```mermaid
flowchart LR
    A[PDF] --> B[Chunking]
    B --> C[Embeddings]
    C --> D[(Chroma<br/>Vector DB)]
    E[Question] --> F[Retriever]
    D --> F
    F --> G[Prompt + Context]
    G --> H[LLM]
    H --> I[Answer]
```

📂 [Repository](https://github.com/svwxyz)

---

### 🔄 On-Prem to Cloud Incremental Data Pipeline
`Azure Data Factory` · `Self-Hosted Integration Runtime` · `SQL Server` · `Azure SQL Database` · `T-SQL` · *Feb 2026*

- Built a hybrid **on-prem SQL Server to Azure SQL Database** migration using a **Self-Hosted Integration Runtime**
- Designed a **watermark-based incremental load**: Lookup the last watermark, Copy only new or updated rows, Lookup the max loaded date, then update the watermark with a **stored procedure**
- Made it **restartable and re-runnable**: the watermark moves only after a successful copy, uses `DATETIME2` precision to avoid data loss, and runs on a **daily schedule trigger**
- Parameterized and reusable across tables (`customer`, `orders`)

```mermaid
flowchart LR
    A[(On-prem<br/>SQL Server)] -->|SHIR| B[ADF Pipeline]
    B --> C[(Azure SQL DB<br/>data_hub)]
    D[(Watermark<br/>table)] <--> B
```

📂 [Repository](https://github.com/svwxyz/OnPrem2CloudDataPipeline)

---

### 🏗️ 30x Data Engineering: Production-Style Pipeline Series
`Azure` · `Databricks` · `Delta Lake` · `Synapse` · `Microsoft Fabric` · *ongoing*

A hands-on series of end-to-end projects, including:

- **Databricks E-commerce Lakehouse**: pipeline built on **medallion architecture** (Bronze, Silver, Gold), documented in its own README
- **Ecommerce Lakeflow Pipeline** and **Retail Delta Lake** projects on Databricks
- **Metadata-driven pipeline** and **back-dated data migration** in Azure Data Factory
- **SQL to Data Lake** production pipeline and a **Sales Data Warehouse**

📂 [Repository](https://github.com/svwxyz/30x-data-engineering)

---

### 📦 More Projects

| Project | Stack | Date |
|---|---|---|
| **Fabric Retail Sales Data Warehouse**: star schema (fact and dimension tables) for sales and revenue analytics | Microsoft Fabric | Mar 2026 |
| **IMDB Data Engineering Pipeline**: ADF ingestion, PySpark transformations in Databricks, Parquet output to Azure Data Lake | ADF, Databricks, ADLS | Sep 2025 |
| **Instagram User Analytics**: SQL analysis of user behavior with Tableau dashboards | SQL, Tableau | Jan 2025 |

---

## 📈 GitHub Stats

<p align="center">
  <img height="180" src="https://github-readme-stats.vercel.app/api?username=svwxyz&show_icons=true&theme=tokyonight&hide_border=true&border_radius=10&include_all_commits=true&count_private=true&rank_icon=github&title_color=7aa2f7&icon_color=bb9af7" />
  <img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=svwxyz&layout=compact&theme=tokyonight&hide_border=true&border_radius=10&langs_count=8&title_color=7aa2f7" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=svwxyz&theme=tokyonight&hide_border=true&border_radius=10" width="75%" />
</p>

### 🏆 Trophies

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=svwxyz&theme=tokyonight&no-frame=true&no-bg=true&margin-w=8&column=7&row=1" />
</p>

### 📊 Contribution Activity

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=svwxyz&theme=tokyo-night&hide_border=true&bg_color=1a1b27&color=7aa2f7&line=bb9af7&point=ffffff&area=true&custom_title=Sumit%27s%20Contribution%20Graph" width="95%" />
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=svwxyz&label=Profile%20views&color=7aa2f7&style=flat" />
</p>

---

<p align="center">
  <i>Always learning, always building pipelines. Let's connect! 🤝</i>
</p>
