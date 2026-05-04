<h2>1. Business Problem</h2>
The objective of this project is to analyze a comprehensive dataset of Canadian oil wells (including Alberta and Saskatchewan) to evaluate production strategies and asset health. The focus is on understanding the performance across different Plays (e.g., Bakken, Montney, Duvernay) and Resource Types (Conventional vs. Tight) to optimize resource management and operational efficiency.  



<h2>2. Business Assumptions</h2>
The analysis is based on the Canadian_Oil_Wells_Enhanced.xlsx dataset. While based on regional well data, specific production volumes and downtime events were modeled to demonstrate end-to-end analytical capabilities suitable for Tundra's Data Analyst role.  



<h2>3. Solution Strategy</h2>
<h4>3.1 Data Acquisition</h4>
Loaded well master data from Canadian_Oil_Wells_Enhanced.xlsx, encompassing dimensions such as UWI, Operator, Field and Play.

<h4>3.2 Data Engineering & Cleaning (Python/Pandas)</h4>
Utilizing Python for ETL ensures scalability and performance, aligning with Tundra’s goal of enabling self-service and AI-ready datasets.  
UWI Standardization: Ensured Unique Well Identifiers (UWI) follow the Canadian regulatory format for precise table joining.
Coordinate Validation: Verified Latitude and Longitude within regional boundaries (AB/SK) to ensure geospatial accuracy.
Status Mapping: Standardized the Status column (e.g., Active, Abandoned, Suspended) to facilitate reliability analysis.
Handling Nulls: Applied logic-based imputation for missing Spud_Date and On_Production_Date to maintain time-series integrity.

<h4>3.3 Optimized Storage</h4>
Exported the refined dataset to .parquet format to optimize storage efficiency and query performance in Power BI, reflecting best practices for large-scale energy data.

<h4>3.4 Power BI Dashboard Development</h4>
Designed a business-critical dashboard focusing on the following core functionalities:  
KPI Visualization: Total Production, Deferred Production, and Runtime Efficiency.
Dynamic Filtering:
Province (Alberta vs. Saskatchewan)
Play (Bakken, Montney, Duvernay, etc.)
Operator (Cenovus, etc.)
Resource Type (Conventional/Tight)
Field (Regional operational areas)

<h4>3.5 Dimensional Modeling (Star Schema)</h4>
Created a centralized Date Dimension table to support time-intelligence DAX functions (YTD, MTD) and built a robust Star Schema connecting the Well Master (Dimensions) to Production Logs (Facts).



<h2>4. Business Questions & Analytics</h2>
<h4>4.1 Which "Play" exhibits the highest density of active completions?</h4>
The analysis identifies the Bakken and Montney plays as the primary drivers of recent activity, with a significant concentration of horizontal wells compared to vertical completions.

<h4>4.2 What is the impact of "Abandoned" vs. "Active" status on regional field performance?</h4>
By segmenting wells by their current Status, the report highlights fields in Saskatchewan that require more aggressive decommissioning strategies versus those ripe for secondary recovery.

<h4>4.3 How does Resource Type (Conventional vs. Tight) affect the production decline curve?</h4>
Tight oil assets show a steeper initial decline rate but higher long-term stability, requiring distinct capital allocation strategies compared to conventional assets.



<h2>5. Business Insights</h2>
<h4>5.1 Play Performance</h4>
The Bakken play in Saskatchewan remains a cornerstone of production efficiency, representing a significant portion of the total active well count in the dataset.

<h4>5.2 Geospatial Clusters</h4>
Mapping the Latitude/Longitude reveals high-density clusters in the Virden and Daly areas (Manitoba/Saskatchewan border), indicating localized infrastructure advantages that Tundra can leverage.



<h2>6. Conclusion</h2>
This Power BI & Python solution provides Tundra’s management with a "single source of truth" for well performance. By translating ambiguous raw data into structured KPIs, the dashboard enables stakeholders to identify production "gaps" and optimize maintenance schedules, directly supporting Tundra’s commitment to sustainable and disciplined growth.
