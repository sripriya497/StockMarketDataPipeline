# StockMarketDataPipeline

Simulated stock data is read from csv file. Randomized data is streamed to Kafka broker by Producer.
Kafka Broker is running on AWS EC2 instance. Consumer read data from kafka topic and stores in S3 bucket.
Glue crawler is used and a table is created for the schema. Amazon Athena is used to run queries on the table for analyses.


![stock_pipeline_diagram](https://github.com/user-attachments/assets/7b1547ca-531a-445f-85d7-d7a88362a7eb)
