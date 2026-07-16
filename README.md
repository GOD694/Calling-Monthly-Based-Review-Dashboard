# Calling Monthly-Based Review Dashboard

A comprehensive Power BI dashboard designed to monitor and analyze call center performance metrics, revenue trends, and agent productivity on a monthly basis.

## 📊 Overview

This dashboard provides real-time insights into call center operations, including call volumes, revenue generation, customer satisfaction, and resolution rates. It enables management to track KPIs, identify trends, and make data-driven decisions.

## 🎯 Key Performance Indicators (KPIs)

### Core Metrics

| KPI | DAX Measure | Description |
|-----|-------------|-------------|
| **Total Calls** | `COUNTROWS(CallData)` | Total number of calls processed |
| **Total Revenue** | `SUM(CallData[Up-sell Amount])` | Total revenue generated from up-sells |
| **Total Up-sells** | `SUM(CallData[Qty of Up-sell])` | Total quantity of up-sell transactions |
| **Avg Call Duration** | `AVERAGE(CallData[Call Duration])` | Average duration of calls in minutes |
| **Avg Satisfaction** | `AVERAGE(CallData[Satisfaction Ratio])` | Average customer satisfaction rating |
| **Resolution Rate %** | `DIVIDE(CALCULATE(COUNTROWS(CallData),CallData[Resolved]="Yes"),COUNTROWS(CallData))` | Percentage of calls successfully resolved |
| **Unique Agents** | `DISTINCTCOUNT(CallData[Agent ID])` | Total number of unique agents |
| **Revenue per Call** | `DIVIDE([Total Revenue],[Total Calls])` | Average revenue generated per call |

## 📈 Dashboard Visualizations

### 1. Total Calls by Region
- **Chart Type:** Clustered Bar Chart
- **Axis:** Region
- **Values:** Total Calls
- **Purpose:** Identify call volume distribution across regions

### 2. Total Revenue by Product
- **Chart Type:** Column Chart
- **Axis:** Product
- **Values:** Total Revenue
- **Purpose:** Track revenue contribution by product line

### 3. Resolution Status
- **Chart Type:** Donut Chart
- **Legend:** Resolved (Yes/No)
- **Values:** Count of Calls
- **Purpose:** Visualize the proportion of resolved vs. unresolved calls

### 4. Satisfaction by Region
- **Chart Type:** Bar Chart
- **Axis:** Region
- **Values:** Average Satisfaction
- **Purpose:** Compare customer satisfaction across regions

### 5. Satisfaction by Product
- **Chart Type:** Column Chart
- **Axis:** Product
- **Values:** Average Satisfaction
- **Purpose:** Identify product-specific satisfaction trends

### 6. Avg Call Duration by Product
- **Chart Type:** Bar Chart
- **Axis:** Product
- **Values:** Average Call Duration
- **Purpose:** Monitor call efficiency by product

### 7. Avg Call Duration by Region
- **Chart Type:** Column Chart
- **Axis:** Region
- **Values:** Average Call Duration
- **Purpose:** Compare call handling times across regions

### 8. Up-sell Revenue Trend
- **Chart Type:** Line Chart
- **Axis:** Date
- **Values:** Total Revenue
- **Purpose:** Track revenue trends over time

### 9. Calls Trend
- **Chart Type:** Line Chart
- **Axis:** Date
- **Values:** Total Calls
- **Purpose:** Monitor call volume trends over time

## 📸 Screenshots

Below are examples of the dashboard visualizations:

### Dashboard Overview
![Dashboard Overview - KPI Cards](./images/dashboard-overview.png)
*Main dashboard view showing all KPI cards including Total Revenue (2M), Total Calls (15K), Average Satisfaction (2.99), Total Up-sells (40K), and Revenue per Call (1.00)*

### Average Call Duration Analysis
![Average Call Duration by Product](./images/call-duration-product.png)
*Average Call Duration by Product showing trend analysis with product-wise breakdown across different regions*

### Regional and Product Analysis
![Regional and Product Calls Analysis](./images/regional-product-analysis.png)
*Total calls by region with detailed product breakdown table showing call distribution across East, Mid-west, North, South, and West regions*

### Complete Dashboard Overview
![Complete Dashboard - Year 2016](./images/complete-dashboard.png)
*Comprehensive dashboard view for 2016 showing all KPIs, regional analysis, revenue trends, call distribution, and satisfaction metrics*

## 📋 Data Model

### CallData Table Structure

The dashboard is built on the following data structure:

- **Agent ID** - Unique identifier for call center agents
- **Call Duration** - Duration of each call (in minutes)
- **Satisfaction Ratio** - Customer satisfaction rating (typically 1-5 scale)
- **Up-sell Amount** - Revenue generated from up-sell
- **Qty of Up-sell** - Quantity of items up-sold
- **Resolved** - Whether the call resolved the issue (Yes/No)
- **Region** - Geographic region of the call
- **Product** - Product category associated with the call
- **Date** - Date of the call

## 🔍 Key Features

✅ **Real-time KPI Tracking** - Monitor all critical metrics at a glance
✅ **Regional Analysis** - Compare performance across different regions
✅ **Product Performance** - Analyze revenue and satisfaction by product
✅ **Trend Analysis** - Visualize performance trends over time
✅ **Quality Metrics** - Track resolution rates and customer satisfaction
✅ **Agent Insights** - Identify unique agent count and performance distribution
✅ **Revenue Metrics** - Monitor up-sell revenue and revenue per call

## 🚀 Usage

1. **Open the Power BI Dashboard** - Launch the Power BI file in Power BI Desktop or Online
2. **Review Monthly Metrics** - Check the KPI cards for current month performance
3. **Analyze Trends** - Use the trend charts to identify patterns and anomalies
4. **Filter by Region/Product** - Use slicers to drill down into specific segments
5. **Export Reports** - Generate monthly reports for stakeholder communication

## 📊 Dashboard Insights

- **Performance Benchmarking** - Compare current metrics against historical performance
- **Regional Performance** - Identify high and low-performing regions
- **Product Analysis** - Determine which products generate the most revenue and satisfaction
- **Agent Productivity** - Track the number of active agents and their collective performance
- **Quality Assurance** - Monitor resolution rates and customer satisfaction scores
- **Revenue Optimization** - Track up-sell trends and revenue per call metrics

## 🔧 DAX Formulas

All KPIs are calculated using standard DAX functions:
- **COUNTROWS** - Count total records
- **SUM** - Aggregate values
- **AVERAGE** - Calculate averages
- **DISTINCTCOUNT** - Count unique values
- **DIVIDE** - Perform safe division with error handling
- **CALCULATE** - Apply filters and conditions

## 📞 Contact & Support

For questions or support regarding this dashboard, please contact the business intelligence team.

---

**Last Updated:** 2026
**Version:** 1.0
**Tool:** Power BI
