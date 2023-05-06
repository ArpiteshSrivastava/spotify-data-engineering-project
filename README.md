# Spotify End-To-End Data Engineering Project

### Project Description:

In this project, we will build an ETL(Extract, Transform, Load) pipeline using the Spotify API on AWS. The pipeline will retrieve data from the Spotify API, transform it to desired format and load it into an AWS data storage service.

### Project Architecture: 
![Architecture Diagram](https://github.com/ArpiteshSrivastava/spotify-data-engineering-project/blob/main/Project%20Architecture%20Diagram.png)


### About Dataset/API Used:
This API contains information about music artist, albums and songs - [Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used:
1. **S3 (Simple Storage Service):** Amazon S3 is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups and static website files.

2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. You can use lambda to run code in response to events like changes in S3, DynamoDB or other AWS services.

3. **Cloud Watch:** Amazon CloudWatch is a monitoring service for AWS resources and the applications you run on them. You can use CloudWatch to collect and track metrics, collect and monitor log files and set alarms.

4. **Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your data sources, identifies data and infer schemas to create an AWS Glue Data Catalog.

5. **Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. You can use the Glue Data Catalog with other AWS services, such as Athena.

6. **Amazon Athena:** Athena is an interactive query service that makes it easy to analyze data in Amazon S3.You can use Athena to analyze data in your Glue Data Catalog or in other S3 buckets.

### Install Packages:
```
pip install pandas
pip install numpy
pip install spotipy
```

### Project Execution Flow
Extract Data From Spotify API -> Lambda Trigger (every 1 hour) -> Run Extract Code -> Store Raw Data -> Trigger Tranform Function -> Tranform Data and Load it -> Query using Athena
