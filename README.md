# RetailAnalytics using Azure 
Certainly! Below is a template for a README.md file summarizing the process you described:

## Overview

This repository contains Python scripts, Azure Data Factory pipelines, and Power BI reports to facilitate the extraction, transformation, and loading (ETL) process from an On-prem MySQL database to Azure Synapse Analytics. The ETL pipeline involves data extraction using Python, transformation of the data, loading it into Azure Blob Storage, and subsequent ingestion into Azure Synapse Analytics using Azure Data Factory.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Folder Structure](#folder-structure)
- [ETL Process](#etl-process)
- [Azure Data Factory Pipeline](#azure-data-factory-pipeline)
- [Power BI Reports](#power-bi-reports)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Ensure that you have the following components set up before running the ETL pipeline:

- Python environment with required dependencies.
- Azure account with Blob Storage and Synapse Analytics resources provisioned.
- Access to the On-prem MySQL database.

## Folder Structure

```
ETL-Project/
|-- src/
|   |-- mysql_to_blob.py
|   |-- azure_data_factory/
|       |-- data_factory_pipeline.json
|-- reports/
|   |-- power_bi_report.pbix
|-- README.md
```

## ETL Process

### Python Script (mysql_to_blob.py)

1. **Database Connection Setup:**
   - Reads database credentials from `config.ini`.
   - Establishes a connection to On-prem MySQL using `mysql.connector`.

2. **User Interaction:**
   - Prompts the user to enter the name of the MySQL table for data extraction.

3. **Query Execution:**
   - Constructs a SELECT query based on the user-specified table.
   - Executes the query using a cursor.

4. **CSV File Creation:**
   - Specifies the output directory as `C:\Users\cmald\Desktop\ETL-Project`.
   - Prompts the user for the desired output CSV file name.

5. **Data Export to CSV:**
   - Writes the header and data rows to the CSV file.

6. **Error Handling:**
   - Catches and prints any `mysql.connector` errors.

7. **Connection Closure:**
   - Closes the cursor and the database connection.

8. **Summary Output:**
   - Prints a success or error message based on the execution.

### Azure Data Factory Pipeline

The Azure Data Factory pipeline (`data_factory_pipeline.json`) orchestrates the process of copying data from Azure Blob Storage to Azure Synapse Analytics.

### Power BI Reports

The Power BI report (`power_bi_report.pbix`) connects to Azure Synapse Analytics to visualize and analyze the loaded data.

## Usage

1. Execute `mysql_to_blob.py` to extract data from On-prem MySQL and store it in Azure Blob Storage.
2. Trigger the Azure Data Factory pipeline to ingest data into Azure Synapse Analytics.
3. Open the Power BI report (`power_bi_report.pbix`) to visualize the data.

## Contributing

Feel free to contribute by opening issues or creating pull requests. Your contributions are welcome!
