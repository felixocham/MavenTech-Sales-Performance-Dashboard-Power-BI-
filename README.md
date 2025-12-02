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

<img width="1258" height="994" alt="image" src="https://github.com/user-attachments/assets/a1a04f30-61a1-4ce0-a8b4-e3572c10a2bf" />


### 2. Key Measures (DAX)
A suite of DAX measures was developed to capture crucial sales performance metrics:

*   **Total Close Value:** `[Total Close Value]`

*   **Won Opportunities:** `[Won Opportunities]`

*   **Average Deal Closure Time:** `[Avg Deal Closure Time (Days)]`

*   **Conversion Rate:** `[Conversion Rate]`

*   **Quarter-over-Quarter Comparison:** Measures for comparing current performance to `PQ (Previous Quarter)`.

### 3. Model Dictionary
A dedicated sheet within the Power BI report serves as a Model Dictionary. This resource documents all technical components:

*   Contents: Tables, Columns, Relationships, and Measures.

*   Details: Name, Description, DAX Expression (for measures), and Location/Source.

<img width="2390" height="1484" alt="image" src="https://github.com/user-attachments/assets/1e990f5a-c783-47ce-9a85-84488323c3dc" />


## Dashboard Features and Views
The dashboard is structured with a navigation system allowing users to switch between six distinct analysis views.

### Global Filters
Persistent filters are available across all views for:

1.   Sales Manager Name

2.   Quarter of Interest

### A. Dashboard View (Summary)
The primary landing page features executive-level KPIs and high-level rankings.

*   **4 KPI Cards:** Total Close Value, Won Opportunities, Average Deal Closure Time, and Total Opportunities.

*   **Ranking Charts:** Top-N analysis for Products and Accounts.

*   **Pipeline Stages:** Chart showing the distribution of deals across various stages (e.g., Prospecting, Engaging, Won, Lost).

*   **Top 5 Matrix:** Comparison of Top 5 Accounts and Top 5 Sales Agents against their Previous Quarter performance.

### B. Account View (Deep Dive)
Focuses on customer performance and characteristics.

*   **Accounts Matrix:** Detailed performance per account (Close Value, Conversion Rate, Avg. Days to Close).

*   **Scatter Plots:**

   *  Close Value by Sector vs. **Account Revenue.**

   *  Close Value by Sector vs. **Number of Employees.**

*   **Ranking Charts:** Ranking of all accounts by Close Value and geographical **Location Ranking** by Close Value.

### C. Period View (Time Intelligence)
Analyses performance trends and quarterly variance.

*   **Charts per Measure:** Visual comparison of performance metrics (Won Opportunities, Avg. Deal Closure Time, Lost Opportunities, Conversion Rate) for the **Current Quarter vs. Previous Quarter (QoQ).**

### D. Product View
Analyses sales performance across the product catalogue.

*   **Charts per Measure:** Breakdown of all key measures for individual products (e.g., how **Conversion Rate** differs between hardware product lines).

### E. Team View
Focuses on sales force effectiveness and regional differences.

*   **Performance Metrics:** Detailed analysis of key measures based on **Individual Sales Staff** and their assigned **Regions.**

### F. Data View (Opportunity Tracker)
A raw data view for investigative purposes.

*   **Opportunity List:** Matrix listing all sales opportunities.

*   **Filtering Buttons:** Allows users to dynamically switch the displayed data between opportunities in various stages: **Prospecting, Engaging, Won, Lost.**
