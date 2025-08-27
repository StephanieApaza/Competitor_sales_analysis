# Competitor Sales Analysis - Manufacturing Industry
This project involves a data analysis of a manufacturing industry, with a special focus on the company Sintec. Sales, product, segment, and geographic data were analyzed, using **Power BI Desktop** for data cleaning, modeling, and visualization.

## 🎯Objetives
- Analyze the market share of Sintec versus competitors.  
- Identify the top-performing products and segments.  
- Evaluate sales growth over time.  
- Build KPIs and dashboards to support strategic decision-making.

## 🧹Data Cleaning & Transformation (Power Query)
Main transformations applied:
1. Replace values and change data type in columns.
2. Append tables.
3. Replace null values.
4. Format dates.
5. Filtered dates to keep only 2019–2021.

## 🧩Data Modeling
- Created a relationship key between Sales and Geography.
- Built a date table for time intelligence.

## 💭Analysis & Key Insights
**Main Competitors**: Artisians was identified as the top competitor in terms of revenue.

**Top Products & Segments**
Category: Urban
Segments: Convenience, Moderation, Extreme
Products:
Sintec: UC-19
General Market: Maximus UM-40

**Growth Over Time**: Sintec experienced strong growth between 2020 and 2021.
And market Share 2021 --> 19.60%

**Year-over-Year Sales Growth**:
Overall growth --> +57.57%
Sintec growth --> +64.71%

## ✅KPIs and DAX Measures
Previous Year Sales (PY Sales): PY Sales = CALCULATE(SUM(Sales[Revenue]),SAMEPERIODLASTYEAR('Date'[Date]))
Revenue Growth %: % Growth = DIVIDE(SUM(Sales[Revenue]) - [PY Sales],[PY Sales])
Sintec Revenue: Sintec Revenue = CALCULATE(SUM(Sales[Revenue]),FILTER(Manufacturer, Manufacturer[ManufacturerID] = 4))

## 📂Files in this Repository
Competitor_sales_analysis - SINTEC.pbix → Power BI project file
images/ → Screenshots of dashboards

## Visualizations
![Dashboard Principal](images/1.%20Dashboard%20-%20Competitor%20sales%20analysis.png)
![Advanced insights](images/2.%20Advanced%20insights.png)
