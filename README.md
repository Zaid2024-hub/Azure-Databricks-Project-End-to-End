# Azure-Databricks-Project-End-to-End

This repository contains a complete end-to-end data engineering project using Azure Databricks, PySpark, and Azure Data Lake Storage. The project demonstrates building a production-grade data pipeline with real-world best practices, designed to help master Azure Databricks and prepare for data engineering roles.

Project Overview
This project implements a modern data engineering pipeline architecture on Azure Databricks following the Medallion architecture pattern (Bronze, Silver, Gold layers). It includes:

Incremental data ingestion using Spark Structured Streaming with idempotency

Data storage using efficient columnar file formats (Parquet)

Data processing with PySpark including advanced functions and Python OOP concepts

Implementation of Slowly Changing Dimensions (Type 1 and Type 2)

Usage of Delta Live Tables for pipeline orchestration and data quality

Data governance and security with Unity Catalog

Integration with SQL warehouses for analytics and BI visualization (e.g., Power BI)

Features
Real-time data ingestion from Azure Data Lake Storage using Autoloader and streaming

Medallion architecture with separated Bronze (raw), Silver (cleaned/enriched), and Gold (consumable star schema) layers

Delta Lake format for ACID transactions and scalable data storage

Slowly Changing Dimension (SCD) handling: Type 1 via code and Type 2 via Delta Live Tables

Reusable PySpark functions and code modularity using Unity Catalog functions

Cluster management and workflow orchestration inside Databricks

Secure cross-resource access setup (Databricks with Data Lake via Azure connector)

Dataset
The project uses a retail dataset that includes tables such as:

Orders

Customers

Products

Regions

The datasets are stored as Parquet files incrementally loaded into the lake.

Project Structure
Azure Resources Setup: Azure Storage Account (Data Lake), Databricks Workspace, Access Connector

Data Lake: Containers for Bronze, Silver, and Gold layers

Notebooks: PySpark notebooks implementing ingestion, transformations, SCD logic, and building star schema

Delta Live Tables: Pipelines for managing SCD Type 2 and automating workflows

SQL Warehouse: SQL endpoints for connecting BI tools like Power BI

Prerequisites
Azure account with Databricks workspace and Data Lake Storage configured

Basic knowledge of PySpark, Delta Lake, and Azure Databricks

Familiarity with data modeling concepts such as star schema and slowly changing dimensions

How to Run
Clone this repository.

Set up Azure resources following the notebooks’ instructions.

Upload the incremental Parquet datasets to the Data Lake source container.

Run the Databricks notebooks in sequence starting from Bronze ingestion to Gold star schema creation.

Deploy Delta Live Tables pipelines for SCD Type 2 management.

Connect SQL warehouses to BI tools for reporting.

Learning Outcomes
Mastery of Azure Databricks ecosystem and features

Hands-on experience with Spark Structured Streaming for real-time data processing

Understanding of Medallion architecture implementation in practice

Building production-ready ETL pipelines with Delta Lake and Delta Live Tables

Implementing data governance with Unity Catalog and secure cloud resource integration

References
Azure Databricks Documentation

Delta Lake Documentation

Unity Catalog Overview

PySpark Official Documentation
