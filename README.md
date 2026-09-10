🍽️ Yummy Delight – Cloud Business Intelligence Project

A complete Business Intelligence project for Yummy Delight, a cloud-kitchen restaurant chain operating across 5 branches in the Muscat Governorate. The project covers a critical evaluation of cloud-based BI, an end-to-end BI architecture design, a comparison of BI tools, and the design of interactive dashboards built in Power BI.

📋 Table of Contents
Overview
Methodology
BI Architecture
BI Tools Comparison
Implementation Roadmap
Dataset
Dashboards
Security & Governance
References
Project Setup
🧭 Overview

Yummy Delight is a cloud-kitchen business operating in 5 different locations within the Muscat Governorate. As a fully digital food business, it generates large volumes of data through:

Its ordering system and mobile app
Delivery partners (Talabat, Careem Now)
Social media and review platforms (Google Reviews, Instagram)

This project aims to turn that data into actionable insights by designing an integrated cloud BI architecture, selecting the most suitable BI tool, and building practical dashboards.

Project Objectives
Critically evaluate the concept of cloud-based Business Intelligence.
Design an end-to-end BI architecture tailored to Yummy Delight.
Compare leading BI tools on the market and select the most appropriate one.
Build 4 interactive dashboards using real-world restaurant data.
🔬 Methodology

The project consists of two main phases:

Phase 1 – Study & Design (Task 1)
Critical Evaluation: Reviewing the literature on cloud-based BI and the role of dashboards in supporting organizational decision-making.
Architecture Design: Proposing a 6-layer functional BI architecture customized for Yummy Delight.
Tool Comparison & Selection: A comparative analysis of 4 major BI tools, with a justified final recommendation and a 6-step implementation plan.
Phase 2 – Practical Application (Task 2)
Using an open-source global restaurant dataset as a realistic proxy for Yummy Delight's operational data.
Loading, cleaning, and processing the data inside Microsoft Power BI.
Building 4 dashboards covering different aspects of operations: geography, cuisine & cost, customer ratings, and services.
🏗️ BI Architecture

The proposed architecture is structured into 6 functional layers, based on best practices from the e-commerce and online food delivery sectors:

#	Layer	Description	Technologies Used
1	Data Sources	Data generation touchpoints: POS, app/website, delivery partners, social media reviews	POS, App/Web, Talabat/Careem API, Google Reviews
2	Data Ingestion	Dual-pipeline ingestion: real-time events + structured data	Apache Kafka (Real-time), AWS Glue (ETL)
3	Cloud Storage	Raw data stored in a Data Lake, aggregated data in a Data Warehouse	AWS S3 (Data Lake), Google BigQuery / AWS Redshift
4	Data Processing	Large-scale data transformation, aggregation, and ML models	Azure Databricks (Apache Spark)
5	BI & Analytics	Analysis, visualization, and predictive analytics	Microsoft Power BI, Azure ML (Python-based Models)
6	Dashboard & Visualisation	Role-based dashboards for branch managers, marketing, and executives	Power BI Web/Mobile

All dashboards are refreshed every 15 minutes to support agile, data-driven decision-making.

Dashboards Proposed in the Architecture
Sales Performance Dashboard
Operations Dashboard
Customer Insights Dashboard
Branch Comparison Dashboard
Marketing ROI Dashboard
⚖️ BI Tools Comparison
Tool	Ease of Use	Cloud Support	Cost	Best For
Microsoft Power BI	High	Native (Azure)	Freemium / Pro (~$20/user/month)	SMEs within the Microsoft ecosystem
Tableau	Medium	Tableau Cloud	Premium (~$70/user/month Creator)	Large enterprises
Google Looker Studio	High	Native (GCP)	Free	Google ecosystem users
Apache Superset	Low–Medium	Self-hosted/Cloud	Open-source	Tech-savvy teams / startups
✅ Recommended Tool: Microsoft Power BI

Power BI was selected for the following reasons:

Best balance of functionality and cost for an early-stage operation.
Natural integration with the Azure cloud services used in the proposed architecture (Hybrid AWS/Azure).
Intuitive UI suitable for branch managers with varying levels of technical expertise.
Support for real-time streaming dashboards to monitor orders live.
Flexible licensing, from the free Desktop version up to Pro.
🛠️ Implementation Roadmap

A 6-step roadmap for implementing the solution using Power BI:

Data Acquisition — Connect Power BI to all data sources (POS API, mobile app database, Talabat/Careem API, Google Reviews scraping tool).
Data Modeling — Build a Star Schema with fact tables (FactOrders, FactSales) surrounded by dimension tables (DimDate, DimBranch, DimMenuItem, DimCustomer).
Data Transformation (ETL) — Use Power Query for data cleansing, currency normalization, date/time parsing, and consistent branch ID mapping.
DAX Measures — Build key metrics: Total Revenue, Average Order Value, Customer Retention Rate, Most Popular Menu Items by Branch, and Net Promoter Score (NPS).
Dashboard Creation — Build 4 dashboards (Sales, Operations, Customer Intelligence, Marketing ROI) using appropriate visuals and the Yummy Delight brand color scheme.
Publishing & Distribution — Publish reports on the Power BI Service, implement Row-Level Security (RLS), and set up automated email report distribution.
📊 Dataset

Since no real operational data for Yummy Delight was available, an open-source global restaurant dataset was used as a realistic representative proxy for the food and cloud-kitchen delivery sector.

Source: 5000 Restaurant Dataset – Kaggle
Key fields: geographic location, cuisine type, cost of food, rating score, number of votes, online delivery availability, table booking status.
Data was loaded into Power BI, cleaned, and processed before building the four dashboards.
📈 Dashboards
Dashboard 1 — Overview & Geography
Visual	Type	Insight
Total number of restaurants & cities	KPI Cards	Scale of the dataset and number of operations
Restaurant locations	Geographic Map	Geographic clustering / density of locations
Top countries by restaurant count	Clustered Bar Chart	Global market penetration
Dashboard 2 — Cuisines & Cost Analysis
Visual	Type	Insight
Most popular cuisines	Treemap	Customer food preferences and industry trends
Average cost for two by currency	Matrix Table	Cost commitment expected of customers by economic zone
Price range distribution	Pie Chart	Distribution of affordable vs. premium restaurants
Dashboard 3 — Customer Ratings & Feedback
Visual	Type	Insight
Rating text distribution	Donut Chart	Quick view of overall brand health and satisfaction
Aggregate rating vs. votes	Scatter Chart	Reliability of high ratings statistically
Top 10 highest-rated restaurants	Clustered Column Chart	Identifying elite venues for benchmarking
Dashboard 4 — Services & Delivery Analysis
Visual	Type	Insight
Table booking availability	Pie Chart	Reliance on advance bookings vs. walk-ins
Online delivery availability	Stacked Bar Chart	Digital readiness of restaurants
Operations directory (name, city, cuisine, rating, delivery)	Matrix/Table	Comprehensive operational reference directory
🔐 Security & Governance

All architecture layers are surrounded by a comprehensive security and governance framework including:

Identity and Access Management (IAM) and Role-Based Access Control (RBAC)
SSL/TLS encryption in transit
AES-256 encryption at rest
Compliance with Oman's Personal Data Protection Law (PDPL) through audit logging and data lineage tracking
