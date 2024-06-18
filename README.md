This project involved the following steps:

- A dataset was sourced from Kaggle and converted to CSV format.
- The CSV dataset was stored in a Git repository.
- An Azure Resource Group was created.
- A Storage account was set up using Data Lake Gen 2.
- Two directories, namely raw-data and transformed-data, were created within the Storage account.
- Data was ingested into Azure from Git using an HTTP request.

Additionally, the following steps were undertaken to implement the project:

- Azure Data Factory was created by accessing the Azure portal and specifying details like name, resource group, and location.
- A linked service for the input task was configured within the Azure Data Factory portal under "Author & Monitor" > "Linked Services" > "HTTP", with details such as name, Git repository URL, and authentication method.
- Datasets were defined for both input and output purposes through "Author & Monitor" > "Datasets" > "New Dataset" > "CSV", linking to the HTTP linked service and specifying the raw data file path.
- A data pipeline was constructed using the "Copy data" method within "Author & Monitor" > "Pipelines" > "New Pipeline" > "Copy data", where source data from the input dataset was copied to the raw-data directory in Data Lake Gen 2.
- The pipeline configuration involved selecting the individual raw data files from the input dataset for the "Copy data" operation.

Following the ingestion and storage of raw data, additional steps were taken for data transformation and analysis:

- **Data Transformation using Databricks:**
  - Data from the raw-data directory in Data Lake Gen 2 was accessed using Databricks.
  - Transformation tasks, such as data cleaning, feature engineering, and aggregation, were performed using Databricks notebooks.
  - Transformed data was saved back to the Data Lake Gen 2 in the transformed-data directory.

- **Data Analysis using Azure Synapse Analytics:**
  - Azure Synapse Analytics was utilized to further analyze the transformed data.
  - Synapse SQL queries and serverless SQL pools were used to query and analyze the transformed datasets.
  - Advanced analytics tasks, such as machine learning model training and predictive analytics, were conducted using the integrated capabilities of Azure Synapse Analytics.

These steps encompassed the end-to-end process of executing the data engineering project, integrating data ingestion, storage, transformation using Databricks, and advanced analytics using Azure Synapse Analytics.
