# Tableau Complete Project End-to-End(Tutorial Project)

Welcome to the **Tableau Complete Project End-to-End** repository!<br>
This project walks through the complete process of data analysis and visualization in Tableau, starting with requirements analysis and ending with fully built dashboards that answer real business questions. It introduces core Tableau functions and tools through the process of building charts and dashboards.

---
## ⚙️Data Architecture
The data architecture for the Tableau Complete Project follows these steps:

![Tableau Project Workflow](docs/diagrams/tableau_project_workflow.png)

---
## 🔗Important Links & Tools:

- **[Datasets](datasets/sales-dashboard-project/datasets)**: Access to the project dataset(csv files).
- **[DrawIO](https://www.drawio.com/)**: Design data architecture, models, flows, and diagrams.
- **[Emojipedia](https://emojipedia.org/en)**: emoji and icon collections
- **[Git Repository](https://github.com/)**: Set up a GitHub account and repository to manage, version, and collaborate on your code efficiently.
- **[Notion](https://www.notion.com/templates/sql-data-warehouse-project)**: Get the Project Template from Notion
- **[SQL Server Express](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)**: Lightweight server for hosting your SQL database.
- **[SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16)**: GUI for managing and interacting with databases.
- **[Tableau Public](https://www.tableau.com/access/download/public)**: Tableau is a visual analytics platform transforming the way we use data to solve problems - empowering people and organizations to make the most of their data.

---

## Project Requirements

### 🔭Analyze Requirements

#### Choose the right charts<br>
For this project, the charts mostly used were 📈line charts and 📊bar charts.

#### Draw Mockup
Refer to pages 6 - 8 in [Dashboard Mockup Diagram](datasets/sales-dashboard-project/project_phases.pdf)

#### Dashboard Color Scheme

**Sales Dashboard**<br>
Below are the colors used in the Sales Dashboard:

| Purpose | Swatch | Hex Code |
|---------|--------|----------|
| Current Year   | ![#212121](https://img.shields.io/badge/-212121-212121) | `#212121` |
| Previous Year  | ![#cecece](https://img.shields.io/badge/-cecece-cecece) | `#cecece` |
| Highest value, above average value | ![#1da2d0](https://img.shields.io/badge/-1da2d0-1da2d0) | `#1da2d0` |
| Lowest value, below average value | ![#ff5500](https://img.shields.io/badge/-ff5500-ff5500) | `#ff5500` |

**Customers Dashboard**<br>
Below are the colors used in the Customers Dashboard:

| Purpose | Swatch | Hex Code |
|---------|--------|----------|
| Current Year   | ![#212121](https://img.shields.io/badge/-212121-212121) | `#212121` |
| Previous Year  | ![#cecece](https://img.shields.io/badge/-cecece-cecece) | `#cecece` |
| Highest value, above average value | ![#59a14f](https://img.shields.io/badge/-59a14f-59a14f) | `#59a14f` |
| Lowest value, below average value | ![#ff9da7](https://img.shields.io/badge/-ff9da7-ff9da7) | `#ff9da7` |
---

### Repository Structure
```
data-warehouse-project/
│
├── datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── docs/                               # Project documentation and architecture details
│   ├── analyse_source_systems.md       # Acquiring relevant information before performing data connections
│   ├── ETL Diagram.png                 # shows all different techniques and methods of ETL
│   ├── data_architecture.png           # shows the project's architecture
│   ├── integration_model.png           # shows how data are connected
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   ├── data_flow_diagram.png           # data flow diagram
│   ├── data_mart.png                   # data models (star schema)
│   ├── naming_conventions.md           # Consistent naming guidelines for tables, columns, and files
│   ├── data_layers.pdf                 # A one-slide-deck reference guide explaining the Bronze/Silver/Gold medallion data architecture — covering each layer's purpose, workflow, and a source-system interview checklist for onboarding new data sources.
│
├── scripts/                            # SQL scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   ├── gold/                           # Scripts for creating analytical models
│
├── tests/                              # Test scripts and quality files
│
├── README.md                           # Project overview and instructions
├── LICENSE                             # License information for the repository

```

---

## License

This project is licensed under the [MIT LICENSE](LICENSE). You are free to use, modify, and share this project with proper attribution.

## About Me

Thanks for visiting! I'm **Mustafa**, an insurance operations professional on a mission to master data analytics and turn raw data into real insights.


[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/mustafa-muntak)
