# SEC Filings Executive Pay End-to-End Project

<img width="1496" height="830" alt="Dashboard" src="https://github.com/user-attachments/assets/d6fedd18-70c3-4cb0-b411-9ab1ee16be8c" />
<img width="1512" height="828" alt="Dashboard2" src="https://github.com/user-attachments/assets/423a366f-f953-41ef-9281-a3434235800e" />
<img width="1594" height="891" alt="Dashboard3" src="https://github.com/user-attachments/assets/d283d207-fd1c-4e48-81d7-af0b6000121a" />

## Objective
This project delivers a fully automated Microsoft Fabric pipeline that ingests SEC DEF14A filings, extracts executive compensation data, enriches it with market information, and powers an interactive Power BI dashboard for executive‑level benchmarking.

The dashboard provides pay‑for‑performance scatterplots, multi‑year CEO compensation boxplots, market‑cap segmentation charts, and percentile pay tables. Peer groups can be filtered by market cap and industry. It enables benchmarking of CEO compensation across thousands of U.S. public companies with updated data once published.

The pipeline includes an incremental ingestion mechanism, which scans for new filings and only adds compensation years from the five-year compensation disclosures not yet included in the database. 

The work was developed in a Fabric workspace without Git integration, requiring a manual export of all notebooks and screenshots.

## Key Features
- Lakehouse Architecture (Bronze → Silver → Gold)  
Clean, layered design ensuring traceability, reproducibility, and separation of concerns.

- Incremental & Parallel Ingestion
Parallel SEC API calls for DEF14A extraction and Yahoo Finance requests for market data. MERGE‑based upserts to avoid duplicates. Year‑level incremental logic for executive compensation (5‑year SCT/PvP tables)

- Automated Data Pipelines  
Modular ingestion and transformation logic, including deduplication, schema validation, and MERGE‑based upserts.

- Data Quality Foundations  
Checks for table existence, schema consistency, null handling and duplicates per CIK + fiscal year.

- Semantic Model for Analytics  
Well‑structured star schema with clear relationships, market-cap segmentation and fiscal-year trend reporting.

- Interactive Power BI Dashboard  
Executive compensation dashboards including pay‑for‑performance scatterplots, multi‑year CEO compensation boxplots, market‑cap segmentation charts, and percentile pay tables.



## Demo & Screenshots
The repository includes:

- A video walkthrough of the dashboard

- Screenshots of the Dashboard, Lakehouse, pipelines, and semantic model

- Exported code and logic for full transparency

## Learnings & Next Steps
Key Learnings:

- Building robust incremental logic for multi‑year compensation tables

- Ensuring schema stability across pipeline runs

## Future improvements could include:

CI/CD integration via Fabric Git mode

- Automated validation rules for XBRL completeness

- Historical backfill of older DEF14A filings

- Additional Gold metrics (TSR deltas, compensation ratios, peer benchmarks)

- Integration with Fabric Data Activator for alerting on new filings
