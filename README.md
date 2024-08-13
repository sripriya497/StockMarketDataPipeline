# StockMarketDataPipeline

Simulated Data is read from csv file and streamed to Kafka broker by Producer.
Kafka Broker is running on AWS EC2 instance. Consumer read data from kafka topic and stores in S3 bucket.
Glue crawler is used and a table is created for the schema. Amazon Athena is used to run queries on the table for analyses.

