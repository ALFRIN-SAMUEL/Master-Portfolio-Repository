# Master Portfolio Repository
1.FINANCIAL DATA EXTRACTION,CLEANING,MANIPULATION AND ANALYSIS OF 4 COMPANIES(AAPL,TSM,MU,AMD)
a) Data pulling
I utilized the yfinance package to obtain 4 years' worth of historical financial data and main financial statements. I programmed the function to loop through the four large firms: AAPL, TSM, AMD, and MU.


b) Data cleaning
I used Pandas to load the uncleaned data in the dataframes to perform the cleaning process as there were four main data frames per company: balance sheet, income statement, historical and cash flow statements.
In order to make a record of the data and have it readily available and clean, I created four different Python dictionaries (balancesheet, incomestatement, cashflows, and history).
During the loop, I cleaned the titles of the columns of the 16 dataframes, that is, four dataframes for each company. Different processes were performed which included removing spaces in the main headers and using the underscore symbol to replace the spaces.This was to ensure that there would be no error while it goes into sql databases.


c) Data warehousing
I created separate databases for each company before running the program (aapl_db, tsm_db, amd_db, and mu_db).Also, I wrote code that allowed me to put these cleaned dataframes into MySQL databases on a company basis where each individual database would contain the 4 distinct tables pertaining to that particular company (for example history_aapl, balance_sheet_aapl, etc).


d) Advanced SQL Analytics in Python
I wrote custom SQL statements directly in Python that would execute via loop and through the pd.read_sql().
I added the results of SQL statements directly into my dictionaries, storing the calculated metrics for each particular company's key (for example balancesheet['AAPL']). The calculated analytics were
•	Balance Sheets: Current Ratio and Debt to Equity ratios to analyze the liquidity of corporations.
•	Income Statement: Gross Profit and Gross Margin percentage
•	Cash Flows: operating, investing, and financing cash flows, free cash flow.


e) Multi-Tab Workbook Creation
I merged all my calculated analytics from dictionaries along with historical prices in Pandas. Then i used openpyxl to make a excel file named financial_analysis_report where each company's analysis was on a separate spreadsheet.


2. E-Commerce Data Pipeline (Python + MySQL + Excel) 
Created an automated data pipeline in Python that programmatically unzipped a compressed ZIP file 
and loaded 540,000+ transactions rows into a MySQL database through SQLAlchemy. 
Used SQL commands to select a selected subset of high-volume transactions
(Country = France and Quantity > 30) and exported them directly into a separate Excel sheet.


3. Practised SQL fundamentals using an Employee Management database, covering CRUD operations, filtering, sorting, constraints, schema modifications, and table joins.
