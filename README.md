1. Business Problem
Tundra Oil & Gas requires clear, trusted insights to enable faster decision-making across its operations in the Western Canadian Sedimentary Basin (WCSB). The objective of this project is to analyze a comprehensive dataset of Canadian oil wells (including Alberta and Saskatchewan) to evaluate production strategies and asset health. The focus is on understanding the performance across different Plays (e.g., Bakken, Montney, Duvernay) and Resource Types (Conventional vs. Tight) to optimize resource management and operational efficiency.  

2. Business Assumptions
The analysis is based on the Canadian_Oil_Wells_Enhanced.xlsx dataset. While based on regional well data, specific production volumes and downtime events were modeled to demonstrate end-to-end analytical capabilities suitable for Tundra's Data Analyst role.  

3. Solution Strategy
3.1 Data Acquisition

Loaded well master data from Canadian_Oil_Wells_Enhanced.xlsx, encompassing dimensions such as UWI, Operator, Field and Play.

3.2 Data Engineering & Cleaning (Python/Pandas)

Utilizing Python for ETL ensures scalability and performance, aligning with Tundra’s goal of enabling self-service and AI-ready datasets.  

UWI Standardization: Ensured Unique Well Identifiers (UWI) follow the Canadian regulatory format for precise table joining.

Coordinate Validation: Verified Latitude and Longitude within regional boundaries (AB/SK) to ensure geospatial accuracy.

Status Mapping: Standardized the Status column (e.g., Active, Abandoned, Suspended) to facilitate reliability analysis.

Handling Nulls: Applied logic-based imputation for missing Spud_Date and On_Production_Date to maintain time-series integrity.

3.3 Optimized Storage

Exported the refined dataset to .parquet format to optimize storage efficiency and query performance in Power BI, reflecting best practices for large-scale energy data.

3.4 Power BI Dashboard Development

Designed a business-critical dashboard focusing on the following core functionalities:  

KPI Visualization: Total Production, Deferred Production, and Runtime Efficiency.

Dynamic Filtering:

Province (Alberta vs. Saskatchewan)

Play (Bakken, Montney, Duvernay, etc.)

Operator (Cenovus, etc.)

Resource Type (Conventional/Tight)

Field (Regional operational areas)

3.5 Dimensional Modeling (Star Schema)

Created a centralized Date Dimension table to support time-intelligence DAX functions (YTD, MTD) and built a robust Star Schema connecting the Well Master (Dimensions) to Production Logs (Facts).

4. Business Questions & Analytics
4.1 Which "Play" exhibits the highest density of active completions?

The analysis identifies the Bakken and Montney plays as the primary drivers of recent activity, with a significant concentration of horizontal wells compared to vertical completions.

4.2 What is the impact of "Abandoned" vs. "Active" status on regional field performance?

By segmenting wells by their current Status, the report highlights fields in Saskatchewan that require more aggressive decommissioning strategies versus those ripe for secondary recovery.

4.3 How does Resource Type (Conventional vs. Tight) affect the production decline curve?

Tight oil assets show a steeper initial decline rate but higher long-term stability, requiring distinct capital allocation strategies compared to conventional assets.

5. Business Insights
5.1 Play Performance

The Bakken play in Saskatchewan remains a cornerstone of production efficiency, representing a significant portion of the total active well count in the dataset.

5.2 Geospatial Clusters

Mapping the Latitude/Longitude reveals high-density clusters in the Virden and Daly areas (Manitoba/Saskatchewan border), indicating localized infrastructure advantages that Tundra can leverage.

6. Conclusion
This Power BI & Python solution provides Tundra’s management with a "single source of truth" for well performance. By translating ambiguous raw data into structured KPIs, the dashboard enables stakeholders to identify production "gaps" and optimize maintenance schedules, directly supporting Tundra’s commitment to sustainable and disciplined growth.
