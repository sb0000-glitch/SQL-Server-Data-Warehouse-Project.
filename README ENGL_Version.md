# Data Architecture: SQL Server & Power BI 

Automated data pipeline construction on SQL Server. Integration of commercial and customer data via a Bronze-Silver-Gold architecture to generate Key Performance Indicators (KPIs) and decision-making dashboards.

Project Goal
This project was born out of ParkAdventure's need to transition from manual management in Excel to an automated Data architecture, in order to identify real growth drivers and prevent customer churn.

To solve this problem, my mission was to build a complete business intelligence solution capable of:
* **Centralizing and Cleaning:** Creating a SQL pipeline (ETL) to transform thousands of raw sales transaction rows into a structured and reliable database.
* **Business Modeling:** Embedding business rules (customer segmentation, product profitability) directly into the code to automate complex calculations.
* **Data-Driven Management:** Delivering an interactive dashboard to transition from manual management in Excel to real-time strategic analysis.

1.Executive Steering & Global KPIs (Overview)

<img width="1376" height="768" alt="Image 1" src="https://github.com/user-attachments/assets/a7bbd9d9-639a-47f4-9254-99f3854fb37b" />

I structured this view to provide an instant snapshot of financial health. 
It relies on joins between the gold.fact_sales fact table and the dimension tables.

* **Global Steering (Finance)**
  * **Key Metrics:** Total Revenue (€29.35M), Order Volume (60K), and Average Order Value.
  * **Impact:** A real-time view of financial health for executive leadership.

* **Customer Analytics (Marketing)**
  * **Segmentation:** Automatic breakdown of 18,480 customers into segments (VIP, Regular, New).
  * **Loyalty:** Recency calculation (inactivity) to identify customers to re-engage before churn.

* **Product Performance (Inventory)**
  * **Top Sales:** Identification of "Champion" products (the Bikes category generates 96% of revenue).
  * **Optimization:** Category analysis to prevent stockouts on the most profitable models.
 
2.Customer Analytics & Segmentation (Customer Overview)

<img width="1360" height="784" alt="Image 2" src="https://github.com/user-attachments/assets/a73c3b3c-3a67-42b0-88a3-69a2e5d8533b" />

This dashboard provides a clear understanding of who the 18,480 customers are and how they spend.

* **Strategic Segmentation:** Automatic grouping of customers into three categories (New, Regular, VIP) based on their purchase history.
* **Loyalty Indicators:** Inactivity calculation (Recency in months) for each "Top 10" customer to spot high-value buyers at risk of churn.
* **Demographics & Geography:** Breakdown by age group and country (with the US market leading at 40%).
* **Trends Over Time:** Sales tracking by segment, highlighting a strong surge in new customer acquisition in 2013.

3.Product Catalog Performance (Product Overview)

<img width="1375" height="784" alt="Image 3 " src="https://github.com/user-attachments/assets/6ac91387-1e6d-443d-aab4-7f3c79de2607" />

This dashboard analyzes the profitability of the 130 active products.

* **Product Segmentation:** Automatic classification into three categories (High, Mid, Low Performer) based on generated revenue.
* **Category Dominance:** Highlighting the Bikes segment, which accounts for 96.46% of total revenue.
* **Top 5 Products:** Identification of "Champion" models (Mountain-200 range) to prioritize stock replenishment.
* **Inactivity Analysis:** Tracking the number of months without sales per product to identify "dormant" items for clearance.
