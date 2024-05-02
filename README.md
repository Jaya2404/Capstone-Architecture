## Overview
This project demonstrates an end-to-end data processing and machine learning pipeline designed for scalability and efficiency. The pipeline integrates several technologies, including Azure Data Lake Storage, Azure Data Factory, and Apache Spark, to process data from initial ingestion to model deployment.

## Architecture
The workflow is divided into several key stages:

### Data Ingestion
- **Input Files**: Data is gathered from various SQL Server databases including tables like Parts Details, Environment Details, Invoice Details, and Master Mapping.
- **Azure Data Factory**: Used for orchestrating and automating the data copying from SQL Server to Azure Data Lake Storage (ADLS).

### Data Processing
- **Bronze Folder**: Stores raw data files copied from on-premises SQL servers to ADLS.
- **Silver Folder**: Data is merged and preprocessed using Spark DataFrames. This stage prepares the data for modeling by handling tasks like merging datasets, converting data types, and cleaning the data.
- **Gold Folder**: Outputs from data processing are stored here, including key features and metrics needed for further analysis and modeling.

### Modeling
- **Model Building**: Leveraging Python and Jupyter notebooks to build predictive models.
- **MLflow**: Used for experiment tracking, model versioning, and deployment.
- **Model Evaluation and Selection**: Critical models are evaluated and the best performing model is selected.

### Deployment
- **Model Serving**: The selected model is deployed to serve predictions.

## Technologies Used
- **Azure Data Lake Storage (ADLS)**: For data storage.
- **Azure Data Factory**: For data orchestration.
- **Apache Spark**: For large-scale data processing.
- **Jupyter/Python**: For model development and experimentation.
- **MLflow**: For managing the machine learning lifecycle, including experiment tracking and model deployment.
