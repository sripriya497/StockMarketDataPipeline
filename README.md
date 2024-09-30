# StockMarketDataPipeline

## Project Description

Designed a data pipeline to ingest stock market data using Kafka on EC2, streaming it to AWS S3. AWS Glue Crawler analyzed the data and created tables in the Glue Data Catalog. Using AWS Athena, I queried the data to extract insights, demonstrating my expertise in AWS and real-time data processing.

Inspiration from [@darshilparmar's](https://github.com/darshilparmar) [data engineering project](https://github.com/darshilparmar/stock-market-kafka-data-engineering-project)

## Architecture

![stock_pipeline_diagram](https://github.com/user-attachments/assets/7b1547ca-531a-445f-85d7-d7a88362a7eb)

## Components

1. **Kafka Producer**: Simulates stock data and streams it to a Kafka broker running on an AWS EC2 instance.
2. **Kafka Broker**: Manages the Kafka topics and handles the data streams.
3. **Kafka Consumer**: Reads data from the Kafka topic and stores it in an AWS S3 bucket.
4. **AWS Glue Crawler**: Analyzes the data in S3 and creates tables in the Glue Data Catalog.
5. **AWS Athena**: Queries the data in the Glue Data Catalog to extract insights.

## Setup Instructions

1. **Kafka Setup**:
   - Install Kafka on an AWS EC2 instance.
   - Configure the Kafka broker and create the necessary topics.

2. **Producer**:
   - Run the [`KafkaProducer.ipynb`](./KafkaProducer.ipynb) notebook to start streaming simulated stock data to the Kafka broker.

3. **Consumer**:
   - Run the [`KafkaConsumer.ipynb`](./KafkaConsumer.ipynb) notebook to consume data from the Kafka topic and store it in S3.

4. **AWS Glue**:
   - Set up an AWS Glue Crawler to analyze the data in S3 and create tables in the Glue Data Catalog.

5. **AWS Athena**:
   - Use AWS Athena to query the data in the Glue Data Catalog and extract insights.

## Usage

- **Data Simulation**: The producer simulates stock market data and streams it to Kafka.
- **Data Ingestion**: The consumer ingests the data from Kafka and stores it in S3.
- **Data Analysis**: AWS Glue Crawler and Athena are used to analyze and query the data.

## Requirements

- AWS Account with access to EC2, S3, Glue, and Athena.
- Python environment with necessary libraries (`pandas`, `kafka-python`, etc.).
- Jupyter Notebook to run the provided `.ipynb` files.
