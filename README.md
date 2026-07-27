# SEC Filings Executive Pay End-to-End Project

<img width="1496" height="830" alt="Dashboard" src="https://github.com/user-attachments/assets/d6fedd18-70c3-4cb0-b411-9ab1ee16be8c" />
<img width="1512" height="828" alt="Dashboard2" src="https://github.com/user-attachments/assets/423a366f-f953-41ef-9281-a3434235800e" />
<img width="1594" height="891" alt="Dashboard3" src="https://github.com/user-attachments/assets/d283d207-fd1c-4e48-81d7-af0b6000121a" />



This project showcases a complete end‑to‑end data solution built in Microsoft Fabric, covering data ingestion, transformation, modeling, and interactive reporting. The objective was to design a scalable, modular, and production‑ready data pipeline capable of processing both intraday stock market data and historical daily data, and delivering near real‑time insights through a Power BI dashboard.

Daily stock data for the five largest U.S. companies was collected from 2011 onward, complemented by minute‑level price data for the current and most recent trading day.
The intraday pipeline refreshes every five minutes, enabling a near real‑time analytics experience.

The work was developed in a Fabric Test Workspace without Git integration, which required a fully manual export of all available assets. To preserve transparency and reproducibility, the repository includes exported notebooks, SQL logic, screenshots of the pipeline and Lakehouse structure, and a demo video of the final dashboard.

## Key Features
- Lakehouse Architecture (Bronze → Silver → Gold)  
Clean, layered design ensuring traceability, reproducibility, and separation of concerns.

- Deployment Pipeline (Dev → Test → Prod)  
Designed a modular promotion flow with deployment rules to ensure stage specific lakehouse connections and parameters .

- Automated Data Pipelines  
Modular ingestion and transformation logic, including deduplication, schema validation, and MERGE‑based upserts.

- Data Quality Foundations  
Checks for table existence, schema consistency, null handling and duplicates.

- Semantic Model for Analytics  
Well‑structured star schema with clear relationships, optimized for performance and maintainability.

- Interactive Power BI Dashboard  
Near real‑time intraday analytics, daily indicators and trend signals, volatility and momentum metrics.



## Demo & Screenshots
The repository includes:

- A video walkthrough of the dashboard

- Screenshots of the Dashboard, Lakehouse, pipelines, and semantic model

- Exported code and logic for full transparency

## Learnings & Next Steps
Key Learnings:

- Understanding Fabric limitations and available workarounds, such as the inability to modify notebook parameters within deployment pipelines rules. Additionally, data source deployment rules for semantic models can only be configured when the semantic model originates from an SQL endpoint.

- Designing scalable Lakehouse architectures, with clear separation between ingestion, transformation, and consumption layers to ensure maintainability and reproducibility.

- Building modular Fabric pipelines, focusing on parallelization, reusable logic, and stage‑aware validation to support future CI/CD integration.

## Future improvements could include:

- CI/CD integration via GitHub or Azure DevOps

- Expanded Data Quality rules and monitoring

- Automated alerting for trend or volatility signals
