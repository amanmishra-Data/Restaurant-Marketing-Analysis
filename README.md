# Restaurant-Marketing-Analysis

# Data Analyst Capstone Project - Marketing (Excel + Tableau)
 ## Tools Used:- Microsoft Excel (for Data Cleaning, Preparation, Basic Analysis)- Tableau (for Visualization and Dashboarding)
 ## 1. Data Preparation in Excel
 ### Step 1: Load and Merge Datasets- Import `data.xlsx_marketing.xlsx` and `Country-Code.xlsx_marketing.xlsx`.- Use VLOOKUP or Power Query to merge on `Country Code` to bring in `Country Name`.
 ### Step 2: Data Cleaning- Remove duplicate rows.- Handle missing values in `Cuisines`, `Aggregate rating`, `Votes`, etc.- Standardize Yes/No values in `Has Table booking` and `Has Online delivery`.- Convert categorical fields into readable format (e.g., 1 = Yes, 0 = No).
 ### Step 3: Feature Engineering- Add a column `Cuisine Count` = COUNT of cuisines by splitting the `Cuisines` column
 using delimiter ",".- Create a new column `Star Restaurant` where:
    =IF(AND([Aggregate rating]>=4.2,[Votes]>=100), "Yes", "No")
 ### Step 4: Save Cleaned Data- Export the final cleaned data to `cleaned_data.xlsx` for Tableau use.
 ## 2. Visualization in Tableau
 ### Step 1: Load Data- Connect Tableau to `cleaned_data.xlsx`.
 ### Step 2: Create Visuals
 #### Scatter Plot - Votes vs Aggregate Rating- X-Axis: Votes- Y-Axis: Aggregate Rating- Size: Cuisine Count- Color: Price Range- Tooltip: Restaurant Name- Insight: Identify star restaurants in the top-right
 #### Highlight Table - Top 10 Star Restaurants- Apply Filters: Votes >= 100, Rating >= 4.2- Columns: Restaurant Name, City, Rating, Votes, Price Range, Cuisine Count, Delivery,
 Table Booking- Sort by: Aggregate Rating (descending)- Use color shading for highlight effect
 #### Bar Charts- Price Range vs Average Rating- Online Delivery vs Average Rating- Table Booking vs Average Rating
#### Heatmap- Cuisine vs City with Average Rating
 ### Step 3: Dashboard- Combine all visuals into one dashboard.- Add filters (Country, City, Price Range).- Highlight KPIs: Total Votes, Avg Rating, Total Star Restaurants.
 ### Step 4: Publish or Export- Save and export the dashboard as PDF or publish to Tableau Public.
