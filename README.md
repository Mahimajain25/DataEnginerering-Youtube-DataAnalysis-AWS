# DataEnginerering-Youtube-DataAnalysis-AWS

- This project aims to securely manage, streamline, and perform analysis on the structured and semi-structured YouTube videos data based on the video categories and the trending metrics.

# Architecture
![Architect](https://drive.google.com/uc?export=view&id=1PHshFfozfLtRpnXmNPWmx9Yfpn-YHISy)

# Dataset 
The Kaggle dataset contains statistics (CSV files) on daily popular YouTube videos over the course of many months. There are up to 200 trending videos published every day for many locations. The data for each region is in its own file. The video title, channel title, publication time, tags, views, likes and dislikes, description, and comment count are among the items included in the data. A category_id field, which differs by area, is also included in the JSON file linked to the region.
[DataSet-Link](https://www.kaggle.com/datasets/datasnaek/youtube-new)

# Approach
- **Data Ingestion :**  Ingest data using AWS CLI ([CLI Commands]()) in AWS S3 bucket.
- **ETL : i)** Extracting the data from S3 bucket and transforming it from json to parquet format using AWS Lamda (auto triggered when file added in S3 bucket) and load the clean data into new s3 bucket. <br>
          **ii)** Glue ETL job to get data fro s3 bucket and transform from csv to parquet format and loading back to new s3 bucket. 
          **iii)** Glue ETL job for joining the two files for final analysis.
          
- **Analysis :** Creating AWS Data Catalog using Crawler and Analysing in AWS Athena.
- **Reporting :** Power BI dashboard for understanding data graphically.

