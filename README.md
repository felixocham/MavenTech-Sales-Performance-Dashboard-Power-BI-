# MavenTech-Sales-Performance-Dashboard (Power BI)
This repository contains the complete Power BI solution developed for MavenTech, a B2B computer hardware sales company, to enable their sales managers **to track and analyse their team's quarterly performance** and gain visibility into sales opportunities currently tracked within their CRM system.
The solution is built on a robust Star Schema Data Model and features an interactive, multi-view dashboard with advanced time intelligence and detailed performance breakdowns across various dimensions (Accounts, Products, Teams, and Time).
### **Key Achievements**
*  Star Schema Implementation: Developed a scalable and efficient data model.

*  Time Intelligence: Enabled quarter-over-quarter and period-based performance comparison.

*  Comprehensive Metrics: Created key performance indicators (KPIs) for closure value, conversion rate, and sales efficiency.

*  Interactive Design: Implemented a multi-page navigation system using bookmarks and buttons for a seamless user experience.

## Technical Details
### 1. Data Model (Star Schema)
   The solution is powered by a well-defined Star Schema to ensure optimal performance and simplified measure development.
   
| Table Name               | Type                | Description                                                        |
| :---                     | :---                | :---                                                               |
| fSalesPipeline           | **Fact**            | Contains individual sales opportunities and core transaction data. |
| dProduct                 | **Dimension**       | Details about the computer hardware products sold.                 |
| dSalesTeam               | **Dimension**       | Information on sales agents, managers, and their regions.          |
| dAccount                 | **Dimension**       | Details on client accounts (e.g., sector, revenue, employees).     |
| dDate                    | **Dimension**       | Dedicated table for time intelligence and calendar operations.     | 
