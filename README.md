Olist E-Commerce Data Pipeline & Performance Analytics 📊
An end-to-end Data Engineering and Analytics project optimizing, structuring, and analyzing Brazil's largest marketplace dataset (Olist) containing millions of interrelated transactional records.

🛠️ Project Architecture & Tech Stack
Data Cleaning & ETL Pipeline: Python (Pandas / Jupyter Notebook)
Relational Database Management: SQL (PostgreSQL / pgAdmin)
Business Intelligence & UI/UX: Tableau
📁 Repository Structure
├── Data_Cleaning_Python/
│   └── Olist_E_Commerce_Data_Cleaning_&_ETL_Pipeline.ipynb  # Pandas data profiling & string handling
├── SQL_Queries/
│   ├── Table_DDL_Schemas.sql                               # Structured table definitions
│   └── Data_Aggregation_Joins.sql                          # Complex multi-table business joins
├── README.md                                               # Technical documentation
└── Project_Dashboard_Video.mp4                             # Walkthrough presentation
⚡ Key Metrics & Business Insights Tracked Executive KPIs: Formulated and tracked Total Revenue ($16.0M) and Total Orders (99K).

Average Order Value (AOV): Engineered custom metrics to analyze regional spending appetite.

Sales Trend Line: Built a dynamic timeline monitoring monthly performance peaks and analyzing commercial seasonality.

Geographical Sales Distribution: Programmed a customized State-level interactive map to pinpoint geographic revenue hubs like São Paulo (SP) and Rio de Janeiro (RJ).

Supply Chain Health: Monitored delivery fulfillment statuses to identify operational delays and logistics bottlenecks.

⚙️ Technical Deep-Dive & Execution 1️⃣ Phase 1: Python ETL Pipeline (Pandas) Data Profiling: Handled inconsistent data, null value distribution, and extreme structural anomalies across multiple raw CSV files.

String Processing & Formatting: Solved encoding issues related to Latin text/Portuguese letters (accents like ã, ç, é) using strict utf-8 normalization techniques.

Data Type Enforcement: Parsed object types into standardized ISO datetime objects to allow seamless time-series trend plotting.

2️⃣ Phase 2: Relational Schema & SQL Optimization (pgAdmin) Designed a clean relational schema joining structural transactional entities across customers, orders, and payments datasets.

Avoided multi-million row duplicate mismatches by applying strict COUNTD and distinct primary key pairing strategies during core query joins.

Optimized aggregations to dynamically serve calculation-heavy KPIs straight into the visualization engine.

⚠️ Real-World Roadblocks & Challenges Overcame 🚨 The SQL Ingestion & Scale Bottleneck Problem: Importing millions of records into pgAdmin using native bulk methods constantly led to server connection timeouts, packet drops, and memory execution freezes.

Solution: Optimized the data ingestion phase by tweaking data-type constraints pre-import, processing files efficiently, and setting structured indexing keys to handle intensive relational query constraints with zero row loss.

🇧🇷 The Language, Domain & Mapping Barrier Problem: Working with international Brazilian data introduced heavy local domain contexts. Over 840 cities initially showed up as "Unrecognized" in Tableau due to mapping mismatches and duplicate naming structures within different regional boundaries.

Solution: Fixed the spatial matching errors by structuring a tight Geographical Hierarchy (Country ➔ State ➔ City) and overriding Tableau’s location mapping to query cities explicitly From Field: customer_state. This filtered out ambiguous entries and achieved a clean 100% data plot rate.

🚀 How to Run this Project Locally

Database Setup (SQL) Open pgAdmin / PostgreSQL.
Execute the schema definitions found in SQL_Queries/Table_DDL_Schemas.sql.

Import the clean datasets into their respective tables.

Analytics Environment Launch the Tableau workbook file or visit the live cloud server link below to interact with the dynamic multi-dashboard pipeline.
