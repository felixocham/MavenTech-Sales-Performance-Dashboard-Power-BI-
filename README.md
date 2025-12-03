# <img width="40" height="40" alt="11232246" src="https://github.com/user-attachments/assets/345f6ba3-cffc-4353-9091-f54dff859be2" /> MavenTech-Sales-Performance-Dashboard (Power BI)
This repository contains the complete Power BI solution developed for MavenTech, a B2B computer hardware sales company, to enable their sales managers **to track and analyse their team's quarterly performance** and gain visibility into sales opportunities currently tracked within their CRM system.
The solution is built on a robust Star Schema Data Model and features an interactive, multi-view dashboard with advanced time intelligence and detailed performance breakdowns across various dimensions (Accounts, Products, Teams, and Time).

### **Key Achievements**
*  Star Schema Implementation: Developed a scalable and efficient data model.

*  Time Intelligence: Enabled quarter-over-quarter and period-based performance comparison.

*  Comprehensive Metrics: Created key performance indicators (KPIs) for closure value, conversion rate, and sales efficiency.

*  Interactive Design: Implemented a multi-page navigation system using bookmarks and buttons for a seamless user experience.

## <img width="40" height="40" alt="12263199" src="https://github.com/user-attachments/assets/bab69a39-a03d-4c6a-8e60-684d6098a590" /> Technical Details

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


## <img width="40" height="40" alt="11264787" src="https://github.com/user-attachments/assets/cfe87b7c-0e4e-4280-bba7-b130ec3ed069" />  Dashboard Features and Views

The dashboard is structured with a navigation system allowing users to switch between six distinct analysis views.

### Global Filters
Persistent filters are available across all views for:

1.   Sales Manager Name

2.   Quarter of Interest

   <img width="2256" height="170" alt="image" src="https://github.com/user-attachments/assets/6280f3a3-99a3-4343-829e-f43aecfb58aa" />


### A. Dashboard View (Summary)
The primary landing page features executive-level KPIs and high-level rankings.

*   **4 KPI Cards:** Total Close Value, Won Opportunities, Average Deal Closure Time, and Total Opportunities.

*   **Ranking Charts:** Top-N analysis for Products and Accounts.

*   **Pipeline Stages:** Chart showing the distribution of deals across various stages (e.g., Prospecting, Engaging, Won, Lost).

*   **Top 5 Matrix:** Comparison of Top 5 Accounts and Top 5 Sales Agents against their Previous Quarter performance.

  <img width="2259" height="1276" alt="image" src="https://github.com/user-attachments/assets/3f9eb594-750e-45ab-8c9a-42b169989001" />


### B. Account View (Deep Dive)
Focuses on customer performance and characteristics.

*   **Accounts Matrix:** Detailed performance per account (Close Value, Conversion Rate, Avg. Days to Close).

*   **Scatter Plots:**

   *  Close Value by Sector vs. **Account Revenue.**

   *  Close Value by Sector vs. **Number of Employees.**

*   **Ranking Charts:** Ranking of all accounts by Close Value and geographical **Location Ranking** by Close Value.

    <img width="2257" height="1273" alt="image" src="https://github.com/user-attachments/assets/8dcb9851-def4-4dd6-b068-dfc5ad9d6bbd" />


### C. Period View (Time Intelligence)
Analyses performance trends and quarterly variance.

*   **Charts per Measure:** Visual comparison of performance metrics (Won Opportunities, Avg. Deal Closure Time, Lost Opportunities, Conversion Rate) for the **Current Quarter vs. Previous Quarter (QoQ).**

    <img width="2255" height="1270" alt="image" src="https://github.com/user-attachments/assets/5da52db2-643a-48c2-a612-e29d6178e43a" />


### D. Product View
Analyses sales performance across the product catalogue.

*   **Charts per Measure:** Breakdown of all key measures for individual products (e.g., how **Conversion Rate** differs between hardware product lines).

    <img width="2253" height="1269" alt="image" src="https://github.com/user-attachments/assets/843e58ab-190f-4890-902d-08722610e653" />


### E. Team View
Focuses on sales force effectiveness and regional differences.

*   **Performance Metrics:** Detailed analysis of key measures based on **Individual Sales Staff** and their assigned **Regions.**

   <img width="2251" height="1273" alt="image" src="https://github.com/user-attachments/assets/e3b525a9-947a-4c03-a878-670997c8cfe4" />


### F. Data View (Opportunity Tracker)
A raw data view for investigative purposes.

*   **Opportunity List:** Matrix listing all sales opportunities.

*   **Filtering Buttons:** Allows users to dynamically switch the displayed data between opportunities in various stages: **Prospecting, Engaging, Won, Lost.**
  
   <img width="2253" height="1268" alt="image" src="https://github.com/user-attachments/assets/d7ab2dff-23d5-4daf-b3bf-21f02587071d" />

## <img width="40" height="40" alt="2499127" src="https://github.com/user-attachments/assets/776f3fb1-3bc6-4818-850d-26647530d4e7" />  Installation and Use
1.   **Clone the Repository:**

```
Bash

git clone (https://github.com/felixocham/MavenTech-Sales-Performance-Dashboard-Power-BI-/edit/main/)
```

2.   **Open the Project:**

      *  Locate the Power BI Desktop file (.pbix) in the repository.

      *  Open the file using **Power BI Desktop.**

3.   **Explore the Report:**

      *  Use the navigation buttons on the top/side of the report canvas to switch between the **Dashboard, Account, Period, Product, Team, and Data** views.

      *  Utilise the global filters for **Manager** and **Quarter** to narrow down the analysis.

4.   **Review the Model:**

      *  Navigate to the dedicated **Model Dictionary** sheet for detailed technical documentation.

## <img width="40" height="40" alt="5406792" src="https://github.com/user-attachments/assets/8691bade-5380-430f-9811-a602111052b6" />  Acknowledgements and Resources

This project was developed as a solution to a community challenge and incorporated design best practices from leading Power BI professionals.

### Challenge Source
Maven Sales Challenge by Maven Analytics

      Link: [https://mavenanalytics.io/challenges/maven-sales-challenge](https://mavenanalytics.io/challenges/maven-sales-challenge)

### Design Inspiration
*   **Next Level Power BI Reports:** Valuable insights on report design, aesthetics, and user experience.

      Channel: [https://www.youtube.com/@nextlevelpowerbireports](https://www.youtube.com/@nextlevelpowerbireports)

*   **How to Power BI:** Techniques and best practices for DAX, data modelling, and report functionality.

      Channel: [https://www.youtube.com/@HowtoPowerBI ](https://www.youtube.com/@HowtoPowerBI) 

---
*Created by Felix Ocham  |  [Linkedin Profile](https://www.linkedin.com/in/felix-o-703987a7/)*

