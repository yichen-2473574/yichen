# Financial Ratio Analysis of Walmart and Costco (2020–2024)

## 1.Problem and User
This project compares the financial performance of Walmart and Costco from 2020 to 2024 using key financial ratios. It is designed for retail investers who want a simple company-level comparison of liquidity and profitability based on annual financial statement data.

## 2.Data
### 2.1Source
  The data comes from WRDS Compustat and was accessed through the  wrds Python package .
**Main tables used:**
- comp.company
- comp.security
- comp.funda


**Access date:2026-04-16**


**Companies included:**
- Walmart (WMT)
- Costco (COST)


**Time period:**
- Fiscal years 2020–2024
### 2.2 Key fields used in the project
- gvkey
- conm
- tic
- datadate
- fyear
- at (total assets)
- ceq (common equity)
- act (current assets)
- lct (current liabilities)
- invt (inventory)
- ni (net income)
- sale (sales)


**The data is filtered to include:**
- industrial format (indfmt = 'INDL')
- standard format (datafmt = 'STD')
- domestic population source (popsrc = 'D')
- consolidated statements (consol = 'C')
## 3. Methods
**The main Python steps in this project are:**
- Connect to WRDS using a personal WRDS account.
- Check available libraries and Compustat tables.
- Retrieve company identifiers for Walmart and Costco.
- Download annual financial statement data from Compustat for 2020–2024.
- Convert dates and sort the dataset by company and fiscal year.
- Check missing values and possible zero denominators before ratio calculation.
- Calculate five financial ratios:
- Create a clean final table for comparison.
- Export the final table to Excel.
- Plot each ratio over time for Walmart and Costco.
## 4. Key Findings
-Walmart and Costco can be directly compared using the same set of liquidity and profitability ratios across five fiscal years.
-The project shows how each company’s ratio values change over time rather than focusing on only one year.
-Using both current ratio and quick ratio gives a clearer view of short-term liquidity.
-Profitability is captured from different angles through net profit margin, ROA, and ROE.
-Visualising the ratios with line charts makes it easier to compare trends between the two companies.

## 5. How to run
- Make sure you have access to WRDS and a valid WRDS username.
- Open the notebook file:notebook.ipynb
- Update the username in the code :username = "your_wrds_username"
- Run the notebook cells in order.
- The final output table will be saved as:financial_ratios_full_table.xlsx
- The charts will be displayed in the notebook.

## 6.Product link / Demo
[Link](https://pan.baidu.com/s/1Cl1WSQh0VJnmPTAg-pJdXQ?pwd=1234)

## 7.Limitations & next steps
  ### 7.1  Limitations 
- This project only compares two companies, so the results should not be treated as a full industry analysis.
- The analysis uses only five years of annual data, which gives a limited time horizon.
- Only a small set of financial ratios is included; other indicators such as debt ratios or efficiency ratios could also be added.
- The project focuses on descriptive comparison and does not apply statistical testing or forecasting methods.
  ### 7.2 Possible next steps
- include more financial ratios
- create subplots to show all ratios in one figure


