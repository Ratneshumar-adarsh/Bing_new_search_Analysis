# Bing_new_search_Analysis
---

# Bing News Sentiment Analysis Pipeline

This project demonstrates an end-to-end data pipeline for ingesting news data using the Bing API, transforming and cleaning the data using **Azure Synapse**, performing sentiment analysis using **Azure Data Science** and **SynapseML**, and visualizing the results in **Azure Databricks**.

## Project Overview

The primary goal of this project is to build an automated pipeline that gathers news data from the Bing API, processes and cleans the data, and performs sentiment analysis to classify the news articles as **positive**, **negative**, or **neutral**. The final results are visualized in a dashboard built using Azure Databricks.

## Workflow

1. **Data Ingestion**:
   - **Source**: Bing API
   - **Tool**: Azure Data Factory (ADF)
   - **Process**: ADF retrieves real-time news articles using the Bing API, processes the JSON response, and loads the data into Azure storage (e.g., Azure Data Lake or Azure Blob Storage).

2. **Data Transformation & Cleaning**:
   - **Tool**: Azure Synapse
   - **Process**: Using Azure Synapse SQL and Apache Spark, the data is cleaned and transformed, including steps like flattening nested structures, handling missing values, and normalizing the dataset.

3. **Sentiment Analysis**:
   - **Tool**: Azure Data Science with SynapseML
   - **Process**: Utilizing **SynapseML**, the cleaned news data is passed through a sentiment analysis model, which classifies the articles into **positive**, **negative**, or **neutral** sentiment.

4. **Data Visualization**:
   - **Tool**: Azure Databricks
   - **Process**: The final sentiment-labeled data is loaded into Azure Databricks, where it is used to create an interactive dashboard. This dashboard provides visual insights into the distribution of sentiments across news articles.

## Key Components

- **Azure Data Factory**: Orchestrates the data pipeline, automates the process of retrieving data from the Bing API, and loads it into Azure storage.
- **Azure Synapse**: Used for data cleaning and transformation, leveraging both SQL and Apache Spark.
- **Azure Data Science**: Used for running machine learning models via SynapseML for sentiment analysis.
- **Azure Databricks**: Final step for data visualization, where an interactive dashboard is created based on the transformed and labeled data.

## Project Steps

1. **Set up Azure Data Factory** to periodically call the Bing API and ingest the data into Azure Blob Storage or Azure Data Lake.
2. **Clean and transform the data** using Azure Synapse, preparing it for further analysis.
3. **Perform sentiment analysis** using SynapseML in Azure Data Science to classify the news as positive, negative, or neutral.
4. **Load the data into Azure Databricks** and create a visual dashboard to display the sentiment analysis results and other insights.

## Tools & Technologies

- **Azure Data Factory**: For data ingestion and orchestration.
- **Azure Synapse**: For data cleaning and transformation.
- **SynapseML**: For machine learning and sentiment analysis.
- **Azure Data Science**: For running ML models and analyzing the data.
- **Azure Databricks**: For data visualization and dashboard creation.
- **Bing API**: As the data source for real-time news articles.

## How to Run the Project

### Prerequisites

- Azure Subscription
- Azure Data Factory, Azure Synapse, Azure Databricks, and Azure Data Science resources set up in your Azure account
- Access to Bing API (API key required)

### Steps

1. **Data Ingestion**:
   - Set up a pipeline in Azure Data Factory to call the Bing API and load the data into Azure Blob Storage.
  
2. **Data Transformation**:
   - Use Azure Synapse to clean and transform the ingested data, handling missing values and flattening nested structures.

3. **Sentiment Analysis**:
   - Run the sentiment analysis using SynapseML in Azure Synapse or Azure Data Science.

4. **Dashboard**:
   - Load the final data into Azure Databricks and create a dashboard using Spark and Databricks visualizations.

## Dashboard Preview

*Attached a pdf named final_bing.pdf*

## Future Enhancements

- Integrate more sophisticated NLP techniques for sentiment analysis.
- Extend the pipeline to include additional sources of data beyond Bing API.
- Build more comprehensive visualizations on the Databricks dashboard.

---
