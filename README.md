# Northwind Modern Data Stack

##  Project Overview

This project demonstrates a complete end-to-end Modern Data Stack implementation, transforming a custom-designed Northwind OLTP database into a fully modeled Analytics Data Warehouse and delivering business-ready insights through interactive Power BI dashboards.

The solution follows industry best practices including:
Design OLTP database from scratch(ERD,Mapping)
-Implementation in Sql server 
-Medallion Architecture (Bronze / Silver / Gold)
-dbt Analytics Engineering
-Slowly Changing Dimensions (SCD Type 2)
-Star & Snowflake schema modeling-Reprting using Power Bi 

##  Project pipeline

![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/DATA%20flow.png?raw=true)


 ### 1. Project Overview & Architecture
The Goal: Transform raw Northwind business data into actionable insights for decision-makers.

The Stack: SQL Server (OLTP), Python (ETL), Airflow (Orchestration), PostgreSQL (DWH), dbt (Transformation), and Power BI (Analytics).

Architecture Diagram: (Include a high-level visual showing the flow from csv → SQL Server → Python → Postgres → dbt → Power BI).


## Phase 1: OLTP Database Design (The Source)
Relational Modeling: Designing the Northwind schema from scratch.

ERD & Mapping: Implementing entities with strict cardinality and participation constraints.

Data Integrity: Implementing Primary Keys, Foreign Keys, and Check Constraints in SQL Server.

Initial Ingestion: Using Bulk Insert to populate the system with CSV data efficiently.

## ERD
![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/ERD.png?raw=true)

## Mapping
![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/MAPPING.png?raw=true)


 ## Phase 2: The Ingestion Layer (Extraction)
Storage Layer: Setting up PostgreSQL as the Target Data Warehouse.

Python ETL: Writing custom Python scripts to bridge the gap between SQL Server and Postgres.

Bronze Layer: Loading "Raw" data into the storage layer without changes to preserve history.

## Phase 3: Data Transformation (dbt & Silver Layer& Gold layer)
Cleaning & Standardization: Removing duplicates, handling nulls, and formatting data.

SCD Type 2 Implementation: Mention how you handled Slowly Changing Dimensions to track historical changes (e.g., changes in employee roles or product prices).

Modular SQL: Writing reusable dbt models to separate logic from final presentation.
## DBT DOCS
![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/dbt%20docs.png?raw=true)

5. Phase 4: Dimensional Modeling (Gold Layer)
Snowflake Schema: Organizing data into Fact and Dimension tables for optimized analytical performance.

Data Quality: implementing dbt tests (unique, not_null, relationship tests) to ensure dareliability.

Documentation: Generating dbt docs and lineage graphs to make the data understandable for others.

## Snowflake Schema
![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/snowflake%20schema.png?raw=true)


## Phase 5: Business Intelligence (The Outcome)
Power BI Connection: Connecting the Gold Layer to Power BI.

DAX Measures: Creating complex calculations (e.g., YTD Sales, Growth %, Customer Retention).
Toolstips and Drill through.
Interactive Dashboards: Visualizing KPIs like "Long-serving vs. High-revenue employees" or "Sales Trends" to support executive decisions.

## Over View
![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/overview.png?raw=true)

## Customer Behavior Analysis

![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/customer%20analysis.png?raw=true)

## Employees Analysis

![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/employees%20analysis.png?raw=true)

## Products Analysis
![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/product%20analysis.png?raw=true)

## Shipper Analysis

![image alt](https://github.com/majedabdualla/Northwind-Modern-Data-Stack/blob/main/schreenshots/shipper%20analysis.png?raw=true)

# Author

## Majed Abdulla
# Aspiring Data Engineer | Analytics Engineer
 # Egypt
 # Linkedin:https://www.linkedin.com/in/majed-abdulla-39ba2438b/


