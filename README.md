# Medallion architecture for FMP news articles

This repo is to record the development of a medallion architecture on AWS for Financial Modeling Prep (FMP) news articles.

FMP is used because it's also used by credible organizations such as Citadel and Harvard.

News articles are used because they're semi-structured data. This is a balance between LLMs being capable of processing unstructured data, and DW methodologies addressing structured data.

The repo has the following files:
- Sample news articles
- Python file for a lambda function that takes articles from FMP and puts into S3
- Notebook that uses a small language model to add more context, then stores the articles in an Apache Iceberg table
- Notebook that reorganizes the data into a star schema around company events that possible have alpha signals

To do:
- Create an agent that answer questions about companies from the gold semantic layer
