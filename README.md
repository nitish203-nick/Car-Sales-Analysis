# Car-Sales-Analysis
Car Sales Performance Analysis & Dashboard
An end-to-end data analytics project that processes raw automotive sales data using Python and translates it into an interactive executive dashboard built in Excel. This project tracks key performance indicators (KPIs), consumer demographics, regional trends, and dealer performance to uncover insights into car sales trends.

📊 Executive Summary & KPIs
Based on the finalized data view shown in Dashboard.png, the dataset tracks thousands of transactions yielding key metrics under filtered scenarios:

Total Revenue: $1,982,159

Average Car Price: $25,090.62

Total Cars Sold: 790 units

Average Customer Income: $831,186.08

📂 Repository Structure
Car Sales.xlsx - car_data.csv: The primary raw dataset containing 23,906 entries and 16 distinct features spanning client demographics, vehicle specs, and dealer locations.

car_da_dashboard.xlsx: The interactive Excel workbook containing the cleaned dataset, structured pivot tables, and the final visualization canvas.

Dashboard.png: A high-resolution screenshot of the operational dashboard canvas.

car_data_analysis.ipynb (or your script name): The Jupyter notebook containing the Python data cleaning and inspection script.

🛠️ Data Pipeline & Process
1. Data Cleaning & Inspection (Python)
Using pandas, numpy, seaborn, and matplotlib, the raw transaction file Car Sales.xlsx - car_data.csv was programmatically audited:

Shape Audit: Confirmed a data matrix of (23,906, 16).

Missing Value Treatment: Checked for nulls across all features using pd.isnull().sum() and safely handled missing values via df.dropna(inplace=True).

Statistical Profiling: Ran descriptive statistics (df.describe()) to capture distributions for Annual Income and Price ($).

Data Export: Processed data was compiled and structured back into an optimized spreadsheet format ready for pivot transformations.

Python
import pandas as pd

# Load the raw dataset 
df = pd.read_csv('Car Sales.xlsx - car_data.csv')

# Drop null values and inspect features
df.dropna(inplace=True)
print(df.isna().sum())

# Export clean version for Excel Dashboard building
df.to_excel("car_data(nitish).xlsx" , index=False)
2. Interactive Dashboard Engineering (Excel)
The clean data was imported into car_da_dashboard.xlsx to establish a relational pivot ecosystem fueling the master user interface:

Dynamic Slicers: Allows instant data cross-examination by Date, Company, Dealer Region, Gender, and Transmission Type.

Sales Metric Tracking: A time-series trend line plotting aggregate sales performance across active distribution periods.

Demographics Breakdown: A breakdown showing customer gender distributions (79% Male vs. 21% Female) paired alongside an Income bracket donut chart.

Body Style Analysis: Multi-angle horizontal and vertical bar charts measuring the sales volumes of SUVs, Sedans, and Hatchbacks.

Leaderboards: Granular performance breakdowns outlining the highest-grossing regions (e.g., Scottsdale, Janesville, Austin) and top-producing dealerships.
