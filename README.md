# A Python Tool for Automated Financial Ratio Analysis Using WRDS Compustat Data(Demonstration cases: Walmart and Costco, 2020–2024)

## 1.Problem and User
This project develops a reusable Python tool that retrieves financial data from WRDS Compustat and calculates five key financial ratios for any retail company. The tool is designed for beginner-level financial analysts and retail investors who want a simple, automated way to compare liquidity and profitability across companies. To demonstrate the tool's functionality, Walmart and Costco are used as case studies for the 2020–2024 period.


## 2.Data
### 2.1Source
  The data comes from WRDS Compustat and was accessed through the  wrds Python package .
**Main tables used:**
- comp.company
- comp.security
- comp.funda


**Access date:2026-04-16**


**Companies included:**
For this demonstration, the tool is applied to:
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
- Retrieve company identifiers (e.g., for demonstration: Walmart and Costco).
- Download annual financial statement data from Compustat for 2020–2024.
- Convert dates and sort the dataset by company and fiscal year.
- Check missing values and possible zero denominators before ratio calculation.
- Calculate five financial ratios:
- Create a clean final table for comparison.
- Export the final table to Excel.
- Plot each ratio over time for Walmart and Costco.
## 4. Key Findings
- A direct comparison of both companies using the same set of liquidity and profitability ratios across five fiscal years.
- Year-over-year trend visualisations for each ratio, showing how each company's performance changes over time.
- Line charts that make it easy to compare trends between two companies within the same industry.
## 5. How to run
- Make sure you have access to WRDS and a valid WRDS username.
- Open the notebook file:notebook.ipynb
- Update the username in the code :username = "your_wrds_username"
- Run the notebook cells in order.
- The final output table will be saved as:financial_ratios_full_table.xlsx
- The charts will be displayed in the notebook.

## 6.Limitations & next steps
### 6.1  Limitations 
- This demonstration only applies the tool to two companies, so the results should not be treated as a full industry analysis.
- The analysis uses only five years of annual data, which gives a limited time horizon.
- Only a small set of financial ratios is included; other indicators such as debt ratios or efficiency ratios could also be added.
- The project focuses on descriptive comparison and does not apply statistical testing or forecasting methods.
 ### 6.2 Possible next steps
- include more financial ratios
- create subplots to show all ratios in one figure


