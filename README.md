# Azure-End-to-End-Project-CarSales-Data
Azure Data Engineering project using Medallion Architecture to process car sales data with Data Factory, Databricks, and Data Lake Gen2. It transforms raw data into analysis-ready datasets, including implementation, notebooks, SQL scripts, and diagrams.
# Architecture Diagram
Below is the architecture diagram illustrating the flow of data through the Medallion Architecture.
![WhatsApp Image 2025-02-02 at 23 12 45_e8911e5d](https://github.com/user-attachments/assets/cd05fd79-c5bc-4f93-b578-038055ba5006)

# Overview
This project showcases the implementation of a Medallion Architecture for a data engineering workflow. The architecture processes raw data, applies incremental data loading, and transforms it into a star schema for analytics using Azure tools.

# Objective
To design and implement a scalable data engineering solution that follows the Medallion Architecture principles, enabling efficient data ingestion, transformation, and analysis.

# Key Features
Implements a Medallion Architecture with Bronze, Silver, and Gold layers for data processing.
Automates data ingestion from GitHub into Azure SQL Database using Azure Data Factory.
Enables incremental data loading into Azure Data Lake Gen 2.
Performs data transformation and cleaning using Azure Databricks notebooks and workflows.
Builds a Star Schema with Fact and Dimension Tables using Databricks workflow and implements SCD Type-1 for analytics-ready datasets.

# Technologies Used
Azure Data Factory (ADF): Orchestration of pipelines for data movement and transformation.
Azure SQL Database: Storage of raw ingested data.
Azure Data Lake Gen 2: Layered storage for Bronze, Silver, and Gold data containers.
Azure Databricks: Data transformation using notebooks and workflows.
Star Schema Design: Fact and dimension tables with SCD Type-1 implementation.

# Project Workflow
## Raw Data Ingestion:
Raw data is sourced from GitHub via HTTPS.
ADF Pipeline 1 ingests data and stores it in Azure SQL Database.
## Incremental Data Loading:
ADF Pipeline 2 handles incremental data loading into the Bronze container in Azure Data Lake Gen 2.
## Data Transformation:
Data is cleaned and transformed using Azure Databricks notebooks.
Transformed data is stored in Silver and Gold containers.
## Star Schema Design and Workflow Execution:
The Dimension Tables and Fact Table are created using Azure Databricks workflow.
SCD Type-1 is implemented for handling updates to dimension tables.

# Pipelines Details
## Pipeline1: Data Ingestion
This pipeline moves raw data from GitHub into Azure SQL Database
![WhatsApp Image 2025-02-02 at 23 22 34_a32558fd](https://github.com/user-attachments/assets/7bd26e73-bd7d-48d2-b090-013ffc4da410)

# Pipeline 2: Incremental Loading
This pipeline manages incremental data loading into the Bronze container
![WhatsApp Image 2025-01-29 at 23 48 00_cdea40bd](https://github.com/user-attachments/assets/57dabef7-b66e-4c63-a369-31f116533489)

