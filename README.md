# RetailAnalytics using Azure 

## Overview

This repository contains Python scripts, Jupyter Notebooks, Azure Data Factory pipelines, and Power BI reports to facilitate the extraction, transformation, and loading (ETL) process from an On-prem MySQL database to Azure Synapse Analytics. The ETL pipeline involves data extraction using Python and Jupyter Notebooks, transformation of the data, loading it into Azure Blob Storage, and subsequent ingestion into Azure Synapse Analytics using Azure Data Factory.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Folder Structure](#folder-structure)
- [ETL Process](#etl-process)
  - [Python Script (mysql_to_blob.py)](#python-script-mysql_to_blobpy)
  - [Jupyter Notebook (Extraction-Part1.ipynb)](#jupyter-notebook-extraction-part1ipynb)
  - [Jupyter Notebook (Transformation (1).ipynb)](#jupyter-notebook-transformation-1ipynb)
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

## ETL Process

### Python Script

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

### Jupyter Notebook (Extraction-Part1.ipynb)

The Jupyter Notebook (`Extraction-Part1.ipynb`) contains the extraction logic for retrieving data from the On-prem MySQL database. It includes interactive code cells and explanations for each step of the extraction process.

Make sure to run the notebook in a Jupyter environment with the required dependencies installed.

### Jupyter Notebook (Transformation (1).ipynb)

The Jupyter Notebook (`Transformation (1).ipynb`) contains the transformation logic for processing and modifying the extracted data. It includes interactive code cells and explanations for each step of the transformation process.

Make sure to run the notebook in a Jupyter environment with the required dependencies installed.

### Azure Data Factory Pipeline

The Azure Data Factory pipeline (`data_factory_pipeline.json`) orchestrates the process of copying data from Azure Blob Storage to Azure Synapse Analytics.

### Power BI Reports

The Power BI report (`power_bi_report.pbix`) connects to Azure Synapse Analytics to visualize and analyze the loaded data.

## Usage

1. Execute `mysql_to_blob.py` to extract data from On-prem MySQL and store it in Azure Blob Storage.
2. Run the Jupyter Notebooks for extraction and transformation in the specified order.
3. Trigger the Azure Data Factory pipeline to ingest data into Azure Synapse Analytics.
4. Open the Power BI report (`power_bi_report.pbix`) to visualize the data.

## Contributing

Feel free to contribute by opening issues or creating pull requests. Your contributions are welcome!

