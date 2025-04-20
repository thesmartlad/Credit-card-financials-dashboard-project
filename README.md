# Credit-card-financials-dashboard-project
Power Bi project


## Credit Card Financial Dashboard (Power BI & SQL)
Hello! This repository contains my work on the Credit Card Financial Dashboard project. I built this end-to-end data analysis solution using Power BI, leveraging data stored in a SQL database. The project involved data extraction, processing, DAX calculations, and creating interactive dashboards to analyze credit card transactions and customer demographics.


## Project Objective
The primary goal was to develop a comprehensive set of weekly credit card dashboards (a Transaction Report and a Customer Report) using Power BI. These dashboards aim to provide real-time insights into key performance indicators (KPIs) and trends, enabling stakeholders to effectively monitor and analyze credit card operations and customer behavior on a weekly basis.


## Dataset & Schema
The analysis utilizes datasets named as "credit card transactions", "customer information", "credit card additional information", "customer additional information"



## Project Workflow & SQL/Power BI Techniques
My process involved several key technical steps:

### 1. Database Setup (SQL):
- Set up a relational database in PostgreSQL.
- Created database tables (cc_details, cust_details) using `CREATE TABLE` statements, defining appropriate column names and data types (`VARCHAR`, `INT`, `DATE`, `DECIMAL`, etc.).
- Imported the initial data from the CSV files into the SQL tables. This involved using database-specific commands like `COPY FROM`, specifying file paths, delimiters (comma), and handling headers.

### 2. Power BI Connection:
- Connected Power BI Desktop to the SQL database using the appropriate connector (Get Data > SQL Server Database or PostgreSQL database).
- Provided server details (localhost or IP address), the database name (where project related data is stored), and authentication credentials (username/password, potentially the PostgreSQL master password).
- Chose Import mode to load data into Power BI's internal model.

### 3. Data Modeling (Power BI):
Established relationships between the imported tables (credit card details and customer details) based on the common key (client_num). This allows for filtering and analysis across both datasets.

### 4. Data Processing & DAX Calculations (Power BI):
- Performed necessary data type corrections or minor transformations within Power Query Editor if needed.
- Created calculated columns and measures using Data Analysis Expressions (DAX) to enhance the analysis:
    
    - Calculated Columns:
       - Age Group: Grouped Customer_Age into buckets (e.g., "20-30", "31-40") using the SWITCH(TRUE(), ...) function for better visualization.
       - Income Group: Similarly grouped Income categories if needed.
       - Month, Year: Extracted from date fields for time-based analysis.

   

    - Measures:
       - Total Revenue: Calculated based on relevant fields (e.g., sum of transaction amounts or specific revenue streams).
       - Total Interest: Sum of Interest_Earned.
       - Total Transaction Amount: Sum of Total_Trans_Amt.
       - Total Transaction Volume: Sum of Total_Trans_Vol.
       - Customer Satisfaction Score: Average of Cust_Satisfaction_Score.
       - Activation Rate (%): Calculated based on Activation_30_Days.
       - Delinquency Rate (%): Calculated based on Delinquent_Acc.
       - Utilized DAX functions like `SUM`, `AVERAGE`, `COUNT`, `DISTINCTCOUNT`, `CALCULATE`, `DIVIDE`, and potentially Time Intelligence functions (`WEEKNUM`, etc.) for weekly comparisons.


## Dashboard Design & Visualization (Power BI):
Designed two interactive dashboards:
   - Credit Card Transaction Report: Focused on financial metrics, transaction volumes, spending types, revenue by card category, etc.
     
   - Credit Card Customer Report: Focused on customer demographics, satisfaction, revenue by gender/age group, top states, etc.


## Key Insights & Recommendations
My analysis using these dashboards revealed several insights:

- Revenue & Transactions: Tracked total revenue which was $57M, total interest $8M, and total transaction amount $44.5M up to the analyzed period (e.g., week 52).

- Customer Demographics: Identified key customer segments (e.g., age group 40-50 are frequent users). Found revenue contribution differences by gender (e.g., Males $31M vs. Females $26M).

- Card Usage: Determined dominant card types (e.g., Blue and Silver account for 93% of transactions) and preferred usage methods is (Swiping).

- Geographic Performance: Identified top contributing states (Texas, New York, California contribute ~68% revenue).

- Operational Metrics: Calculated overall customer satisfaction rate i.e 3.20


## Based on these insights, potential recommendations include:
- Target marketing campaigns towards the 40-50 age group.

- Promote benefits of preferred usage methods (like swiping).

- Develop strategies for regions with lower revenue contributions.

- Implement initiatives to decrease the delinquency rate.

- Enhance rewards for dominant card types (Blue/Silver) to maintain loyalty.


## Technologies Used
- SQL: For database creation, data storage, and initial querying/setup (using PostgreSQL or MySQL).

- Power BI Desktop: For data connection, data modeling, DAX calculations, creating interactive visualizations, and dashboard design.

- DAX (Data Analysis Expressions): For creating calculated columns and measures within Power BI.

- Excel: For viewing and understanding the raw CSV data.







