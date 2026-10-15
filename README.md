📊 Power BI Data Modeling | From Raw Data to an Analytical Model
   
Turning scattered business data into a structured, analysis-ready Power BI model.

✨ Project Overview
This project focuses on data modeling in Microsoft Power BI. Starting with an Excel workbook containing multiple business datasets, the goal was to reorganize the data into a clearer analytical structure, separating fact tables from dimension tables and defining relationships that support reporting and analysis.
The project includes a Power BI .pbix file, the original Excel dataset, and screenshots comparing the model before and after restructuring.

🔄 Before & After: Model Transformation
Before — Source-oriented model

The starting model contained source-oriented tables for orders, customers, products, invoices, payments, shipments, inventory, campaigns, and more. This made the model harder to navigate and reason about.
After — Structured analytical model

The redesigned model groups analytical data into clearly named fact and dimension tables, with a dedicated date dimension and a separate measures table. The screenshot also shows active and inactive relationships used for different analytical paths.
🧱 Data Model Architecture
Layer	Tables visible in the final model	Purpose
Facts	fact_sales, fact_order_process, fact_inventory, fact_campaign_spend, fact_promotion_coverage, fact_sales_targets	Capture sales, order processes, stock, marketing activity, promotions, and targets
Dimensions	dim_customer, dim_product, dim_campaign, dim_geo, dim_order_flags, dim_date	Provide descriptive attributes for slicing and filtering
Supporting	_measures, security	Organize DAX measures and regional security-related data


The final design uses star-schema principles, with multiple fact tables sharing dimensions where appropriate. It is best described as a multi-fact analytical model, rather than a single textbook star schema.
🛠️ Skills & Techniques Demonstrated
- Power Query: preparing and reshaping source data for modeling.
- Dimensional Modeling: separating business events and numeric measures from descriptive attributes.
- Data Relationships: configuring one-to-many relationships and managing multiple date paths.
- Date Dimension: supporting calendar-based analysis through dim_date.
- DAX Organization: maintaining calculations in a dedicated _measures table.
- Business Data Integration: connecting sales, customers, products, inventory, marketing, and order operations in one analytical model.
🎯 Business Questions the Model Can Support
- How do sales change by month, year, product, or region?
- Which customer segments and products contribute to revenue?
- How does inventory vary across products and periods?
- How does campaign spending relate to promotional activity?
- How do actual sales compare with revenue targets?
- What are the differences between order, invoice, shipment, and delivery dates?
These are potential analysis use cases enabled by the model, not claims that every report or metric is already implemented.
📂 Repository Structure
data_modeling_project/
├── data_model_project.pbix      # Power BI project
├── dataset.xlsx                # Source workbook
├── Screenshot/
│   ├── before.png              # Original model
│   └── after.png               # Restructured model
└── README.md                   # Project documentation
🚀 How to Explore the Project
1. Download or clone this repository.
2. Open data_model_project.pbix using Power BI Desktop.
3. Switch to Model view to explore fact tables, dimensions, and relationships.
4. Review the screenshots above to compare the original and restructured models.
5. If you need to refresh the source data, update the workbook path in Power Query to point to your local copy of dataset.xlsx.
📌 Key Takeaway
A good data model is the foundation of reliable analytics. By organizing source tables into reusable facts and dimensions, the model becomes easier to understand, extend, and use across business reporting scenarios.
🧰 Tools
Microsoft Power BI Desktop · Power Query · DAX · Microsoft Excel
👤 Author
Alaa Ayman Hijazi
Data Analytics Portfolio Project
⭐ If you find this project useful, feel free to star the repository!
