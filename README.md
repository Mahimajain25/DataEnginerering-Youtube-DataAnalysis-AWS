# DataEnginerering-Youtube-DataAnalysis-AWS

- This project aims to securely manage, streamline, and perform analysis on the structured and semi-structured YouTube videos data based on the video categories and the trending metrics.

# Architecture
![Architect](https://drive.google.com/uc?export=view&id=1PHshFfozfLtRpnXmNPWmx9Yfpn-YHISy)

# Dataset 
The Kaggle dataset contains statistics (CSV files) on daily popular YouTube videos over the course of many months. There are up to 200 trending videos published every day for many locations. The data for each region is in its own file. The video title, channel title, publication time, tags, views, likes and dislikes, description, and comment count are among the items included in the data. A category_id field, which differs by area, is also included in the JSON file linked to the region.
[Dataset-Link](https://www.kaggle.com/datasets/datasnaek/youtube-new)

# Approach
- **Data Ingestion :**  Ingest data using AWS CLI ([CLI Commands](https://github.com/Mahimajain25/DataEnginerering-Youtube-DataAnalysis-AWS/blob/main/CLI%20Command.txt)) in AWS S3 bucket.
- **ETL : i)** Extracting the data from S3 bucket and transforming it from json to parquet format using AWS Lamda (auto triggered when file added in S3 bucket) and load the clean data into new s3 bucket. ([Lamda Code](https://github.com/Mahimajain25/DataEnginerering-Youtube-DataAnalysis-AWS/blob/main/Lamda%20Code%20JSONtoParquet.txt))  <br>
          **ii)** Glue ETL job (PySpark) to get data from s3 bucket and transform from csv to parquet format and loading back to new s3 bucket. ([PySpark Code](https://github.com/Mahimajain25/DataEnginerering-Youtube-DataAnalysis-AWS/blob/main/Pyspark%20Code%20CSVtoParquet.txt)) <br>
          **iii)** Glue ETL job for joining the two files for final analysis.
- **Analysis :** Creating AWS Data Catalog using Crawler and Analysing in AWS Athena.
- **Reporting :** Power BI dashboard for understanding data graphically.
![utubePowerBI](https://drive.google.com/uc?export=view&id=1kTjhxNxHZ5R1-Xa93uemerj56yzfx0Uf)

# AWS Services used
- **Amazon S3:** Amazon S3 is an object storage service that provides manufacturing scalability, data availability, security, and performance.
- **AWS IAM:** Identity and access management which enables us to manage access to AWS services and resources securely.
- **AWS Glue:** A serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development.
- **AWS Lambda:** Lambda is a computing service that allows programmers to run code without creating or managing servers.
- **AWS Athena:** Athena is an interactive query service for S3 in which there is no need to load data it stays in S3.

## **Technologies used**
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Spark](https://img.shields.io/badge/Apache_Spark-FFFFFF?style=for-the-badge&logo=apachespark&logoColor=#E35A16)

## **Tools used**
![AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![PowerBI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=white)

## Contact

- linkedin - https://www.linkedin.com/in/mahima-jain-41b540191/
- gmail - mahimaj25@gmail.com
