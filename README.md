# Electronic Sales and Reviews Analysis

An end-to-end data pipeline for an electronics retailer: cleaning a year of daily sales data and a raw customer-reviews text file with Python, storing everything in a MySQL database, and building an interactive Power BI dashboard with NLP-based sentiment scoring — from messy source files to a business-ready dashboard.

## Overview

This project combines two very different raw sources — a sales CSV and a plain-text customer reviews file — into one connected analysis. Python handles the cleaning and the sentiment extraction, MySQL (via Xampp) stores the data, and Power BI ties it all together with DAX for the final dashboards.

## Repository structure

├── Cleaning code/
│ ├── sales_cleaning.py # cleans and prepares the raw sales dataset
│ └── nlp_code.py # keyword-based sentiment scoring on the raw reviews text
├── Dataset before cleaning/ # original, unprocessed source files
├── Dashboard/
│ └── Electronic Sales and Reviews Dashboard.pdf # final Power BI dashboards (Sales + Reviews)
└── Report/
└── Project Rahaf Alrehaili.pdf # detailed write-up of the cleaning, database, and modeling process — see pages 7–8 for the full analysis and recommendations

## Tools
- Python (Pandas) — data cleaning and NLP
- MySQL / Xampp — database creation and storage
- Power BI (Power Query, DAX) — data modeling and dashboards

## What I did
- Cleaned and prepared the raw sales data using Python: handled missing values, fixed data types, removed duplicates, and standardized dates
- Built a keyword-based NLP script to score customer reviews as positive/negative sentiment from raw text
- Created and populated a MySQL database (via Xampp) to store product, payment, and rating data, then linked it to the cleaned datasets
- Modeled the relationships between Sales, Reviews, and Product tables in Power BI
- Used DAX to auto-categorize products into groups (Laptops, Smartphones, Televisions, Headphones, Cables, Batteries, Home Appliances) and to generate readable sentiment labels
- Built two interactive Power BI dashboards — Sales and Reviews — with filters by city, month, category, and payment method

## Key findings
- 29K orders analyzed · 34K units sold · $6M in total sales tracked
- Top 3 products by revenue: MacBook Pro Laptop, iPhone, and ThinkPad Laptop
- San Francisco led total sales by city, ahead of Los Angeles and New York City
- Customer sentiment: ~76% positive, ~18% neutral, ~5% negative across reviews
- Batteries showed an unusually high return rate relative to other sub-categories — flagged as worth investigating further

