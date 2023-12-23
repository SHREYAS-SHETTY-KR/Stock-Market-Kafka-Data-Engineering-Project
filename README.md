# Stock-Market-Kafka-Data-Engineering-Project

## Project Overview
The aim of this project is to establish a robust end-to-end data engineering pipeline for ingesting, processing, and querying real-time stock market data using Apache Kafka and various AWS services, including S3, Glue, Athena, and EC2. The pipeline is designed to simulate and analyze stock market data, providing a comprehensive solution for real-time data ingestion, storage, and querying.

## Architecture Diagram
   <img src="Images/Architecture.jpg">

## Services Used
1. **Apache Kafka :** It is an open-source distributed streaming system used for stream processing, real-time data pipelines, and data integration at scale.
2. **Amazon EC2 :** Amazon Elastic Compute Cloud (Amazon EC2) is a web service offered by Amazon Web Services (AWS) that provides resizable compute capacity in the cloud. It allows users to launch and manage virtual servers, known as EC2 instances, to run applications and workloads.
3. **Amazon S3 (Simple Storage Service) :** Amazon S3 is an object storage service known for its manufacturing scalability, data availability, security, and performance.
4. **AWS Glue Crawler :** AWS Glue Crawler is a fully managed service that automatically crawls the data sources, identifies data formats and infers schemas to create an AWS Glue Data Catalog.
5. **AWS Glue Data Catalog :** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. We can use the Glue Data Catalog with other AWS services, such as Athena
6. **AWS Athena :** Athena is an interactive query service that makes it easy to analyze data in amazon s3 using standard SQL. We can use Athena to analyze data in Glue Data catalog or in other s3 buckets

These services are integral to our project and will collectively support our data processing, storage, analysis, and reporting needs in an efficient and scalable manner.

## Dataset
The project utilizes a stock market dataset, available [here]()

## Project Execution Flow

### Setting Up EC2 Instance

**Step 1 :** Launching an EC2 Instance
Deploy an EC2 instance with default configurations and establish a Security Group for internet accessibility.

**Step 2 :** Logging in to the Instance using SSH
Download the primary key, relocate it to the project directory, and establish an SSH connection to the instance.

### Installing and Configuring Required Packages
**Step 3 :** Installing JAVA on EC2
Install JAVA on the EC2 instance using provided commands.

**Step 4 :** Downloading Kafka
Download and extract Kafka onto the EC2 instance.

### Kafka Setup
**Step 5 :** Launching Zookeeper
Start Zookeeper to manage Kafka configurations.

**Step 6 :** Initializing Kafka Server
Initialize the Kafka server on the EC2 instance.

**Step 7 :** Creating a Kafka Topic
Create a Kafka topic to handle the stock market data.

**Step 8 :** Activating the Producer
Launch the Kafka producer to simulate real-time data generation.

**Step 9 :** Initiating the Consumer
Start the Kafka consumer to consume and process the generated data.

### Python Code for Data Generation and Consumption

**Step 10 :** Python Code for Data Generation (Producer)
Launch a Jupyter Notebook, install kafka-python, and script the producer code.

**Step 11 :** Python Code for Data Consumption (Consumer)
In a separate notebook, introduce the consumer using provided statements.

### Data Storage and Processing
**Step 12 :** Write Data to AWS S3
Install the s3fs package and use Python code to write data to an S3 bucket.

**Step 13 :** Implementation of AWS Glue Crawler
Create a Glue Crawler to index metadata from the S3 bucket and create a Glue Data Catalog.

### Data Querying

**Step 14 :** Leveraging AWS Athena for Data Querying
Use AWS Athena to query the stock market data stored in the Glue Data Catalog.

## Conclusion

This project establishes a comprehensive real-time stock market data ingestion pipeline, integrating Apache Kafka for data streaming and various AWS services for storage, processing, and querying. The detailed steps cover setting up the infrastructure, configuring Kafka, generating and consuming data, storing it in S3, and querying it using Athena. The end-to-end pipeline provides a scalable and efficient solution for handling real-time financial data in a cloud environment.
