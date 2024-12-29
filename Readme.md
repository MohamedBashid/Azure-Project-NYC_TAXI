### NYC_TAXI Azure Data Engineering Project

## Project Overview:
This project demonstrates the process of building a Data Engineering pipeline in Azure for the NYC Taxi dataset. The project utilizes Azure Data Factory (ADF) for data extraction and orchestration, Azure Data Lake Gen2 for data storage, Azure Databricks for data transformation, and Power BI for data visualization. The pipeline extracts raw data from an external Parquet dataset and processes it through multiple stages (Bronze, Silver, Gold) in an efficient and scalable manner.

## Key Features: 
**Data Ingestion:** Extracts raw data from an external HTTPS URL using Azure Data Factory and stores it in Azure Data Lake Gen2 (Bronze container). \
**Data Transformation:** Transforms raw data in Azure Databricks and stores the transformed data in the Silver container in Parquet format. \
**Data Aggregation:** Aggregates and refines the data, storing the final, curated dataset in the Gold container in Delta table format. \
**Data Visualization:** Connects the curated data in the Gold container to Power BI Desktop for reporting and visualization. 

## Architecture:
**1. Data Ingestion** (Bronze Container) 
* Azure Data Factory (ADF) is used to create a dynamic pipeline that extracts raw Parquet data from an external HTTPS URL. 
* The extracted data is then copied into the Azure Data Lake Gen2 Bronze container for raw storage.
  
**2. Data Transformation** (Silver Container) 
* Azure Databricks is used to process and transform the raw data stored in the Bronze container. 
* Data transformation involves data cleaning, filtering, and enriching the raw dataset. 
* The transformed data is saved in Parquet format in the Silver container.
  
**3. Data Aggregation and Refinement** (Gold Container) 
* The transformed data from the Silver container is further aggregated and refined to meet business requirements. 
* The final curated dataset is stored in the Gold container in Delta table format, allowing for ACID transactions, versioning, and fast querying.
  
**4. Data Visualization** 
* The data stored in the Gold container is connected to Power BI Desktop for data analysis, reporting, and visualization. This enables stakeholders to generate interactive dashboards and insights from the curated dataset.

## Technology Stack: 
**Azure Data Factory (ADF)** – For orchestrating the data pipeline and extracting data from external sources. \
**Azure Data Lake Gen2** – For storage of raw, transformed, and curated datasets (Bronze, Silver, Gold containers). \
**Azure Databricks** – For transforming and processing data using Apache Spark. \
**Power BI Desktop** – For data visualization and reporting. \
**Delta Lake** – For efficient data storage and querying in the Gold container. \
**Azure Key Vault** - To store the confidential secrets

## Conclusion:
This project showcases an end-to-end Azure Data Engineering pipeline that extracts, transforms, and loads (ETL) data from raw external sources into structured data for business insights. The integration of Azure Data Factory, Databricks, Azure Data Lake Gen2, and Power BI allows for a highly scalable and maintainable data pipeline that provides actionable business insights.
