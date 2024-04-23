This is an end-to-end data engineering project 

1. Sourced a dataset from Kaggle and converted it to CSV format.
2. Saved the dataset in a Git repository.
3. Created an Azure Resource Group.
4. Created a Storage account using Data Lake Gen 2.
5. Created two directories in the Storage account: raw-data and transformed-data.
6. Ingested data from Git using an HTTP request.

*Step 1: Create an Azure Data Factory*

- Go to the Azure portal and create a new Data Factory resource.
- Fill in the required details, such as name, resource group, and location.

*Step 2: Create a linked service for the input task*

- In the ADF portal, click on "Author & Monitor" and then "Linked Services".
- Click on "New Linked Service" and select "HTTP".
- Fill in the required details, such as name, URL (your Git repository URL), and authentication method.

*Step 3: Create datasets for input and output*

- Click on "Author & Monitor" and then "Datasets".
- Click on "New Dataset" and select "CSV".
- Fill in the required details, such as name, linked service (the HTTP linked service you created), and file path (the raw data file path).

*Step 4: Create a data pipeline using the Copy data method*

- Click on "Author & Monitor" and then "Pipelines".
- Click on "New Pipeline" and select "Copy data".
- Fill in the required details, such as name, source (the input dataset), and sink (the raw-data directory in the Data Lake Gen 2).
- Select the Copy data method for individual raw data files.

*Step 5: Assign the source and sink destinations*

- In the pipeline, click on the "Source" tab and select the input dataset.
- Click on the "Sink" tab and select the raw-data directory in the Data Lake Gen 2.

*Step 6: Copy data method for individual raw data files*

- In the pipeline, click on the "Copy data" tab.
- Select the "File" option and choose the individual raw data files from the input dataset.

That's it! You've created an Azure Data Factory pipeline to ingest data from your Git repository and store it in the raw-data directory of your Data Lake Gen 2.
