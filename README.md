# Spotify-End-to-End-Data-Engineering-Project

### Introduction
In this project, we will build an ETL(Extract, Transform, Load) pipeline using the Spotify API on AWS. The pipeline will retrieve data from the Spotify API, transform it to a desired format, and load it into an AWS store.

### Architecture
![Spotify DE AWS architecture](https://github.com/Bhargav1234567/Spotify-End-to-End-Data-Engineering-Project/blob/main/Architecture.jpeg)

### About Dataset/API
This API contains information about music artist, albums and songs - [Spotify API](https://developer.spotify.com/documentation/)

### Services Used
1. **S3(Simple Storage Service)**: Amazon Simple Storage Service (S3) is a highly scalable, secure, and durable object storage service designed for storing and retrieving any amount of data via the internet.
2. **AWS Lambda**: AWS Lambda is a serverless, event-driven compute service that allows you to run code without provisioning or managing servers.
3. **Cloud Watch**: Amazon CloudWatch is a comprehensive monitoring and observability service for AWS resources and applications. It collects monitoring data in the form of logs, metrics, and events, providing actionable insights to optimize performance and automate operational tasks.
4. **Glue Crawler**: An AWS Glue Crawler automatically scans data in sources like S3, JDBC, or DynamoDB, infers schemas, and populates the AWS Glue Data Catalog with metadata.
5. **Glue Catalog**: The AWS Glue Data Catalog is a centralized, serverless metadata repository for all data assets within an organization, both on-premises and in the cloud.
6. **Amazon Athena**: Amazon Athena is a serverless, interactive query service that makes it easy to analyze data directly in Amazon S3 using standard SQL.

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```
### Project Execution Flow
Extract Data from API -> Lambda Trigger(every 1 hour) -> Run Extract Code -> Store Raw Data -> Trigger Transform Function -> Transform Data and Load it -> Query Using Athena
