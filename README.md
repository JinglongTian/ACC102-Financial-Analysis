# Financial Analysis Product: Coca-Cola vs. PepsiCo (2015-2025)

## 1. Problem & User
This project compares the profitability and financial health of Coca-Cola (KO) and PepsiCo (PEP) to help business students understand how different operational models impact financial ratios. It specifically addresses whether Coca-Cola's asset-light strategy results in superior margins compared to PepsiCo's integrated model.

## 2. Data
* **Source:** WRDS (Wharton Research Data Services) - Compustat North America.
* **Access Date:** April 25, 2026.
* **Key Fields:** `tic` (Ticker), `fyear` (Fiscal Year), `revt` (Revenue), `ni` (Net Income), `at` (Total Assets), `lt` (Total Liabilities).

## 3. Methods
1.  **Data Acquisition:** Established a connection to the WRDS server via the `wrds` library and used SQL to extract financial data for 'KO' and 'PEP'.
2.  **Data Cleaning:** Handled missing values using `dropna()` and ensured correct data types for calculation.
3.  **Transformation:** Calculated Net Profit Margin (`ni/revt`) and Leverage (`lt/at`) using `pandas` vectorized operations.
4.  **Analysis:** Aggregated data into comparison matrices using `pivot_table()`.
5.  **Visualization:** Generated comparative line charts and bar charts using `matplotlib` to illustrate trends.

## 4. Key Findings
* **Profitability Gap:** Coca-Cola consistently maintains a significantly higher Net Profit Margin than PepsiCo, often double the percentage.
* **Model Efficiency:** The data confirms that Coca-Cola's focus on high-margin concentrate sales is more profitable than PepsiCo's capital-intensive snack and beverage manufacturing.
* **Leverage Stability:** Both companies exhibit stable debt-to-asset ratios, though PepsiCo's leverage is slightly higher due to its larger physical infrastructure requirements.
* **Strategic Insight:** For investors, Coca-Cola offers higher efficiency, while PepsiCo offers broader portfolio diversification despite lower margins.

## 5. How to run
1.  Open `notebook.ipynb` and enter your WRDS credentials when prompted by `wrds.Connection()`.
2.  Ensure the SQL query in the notebook is targeting the `comp.funda` table.
3.  Run all cells from top to bottom to reproduce the tables and figures.

## 6. Product link / Demo
* **Video Demo:** See the link at the top of this README.
* **Analysis Workflow:** Detailed code and reasoning are available in the `notebook.ipynb` file in this repository.

## 7. Limitations & next steps
* **Limitations:** The analysis is limited to two companies and relies on standard accounting figures that may not capture specific regional economic impacts.
* **Next Steps:** Future work could incorporate cash flow analysis or use the `yfinance` library to correlate these financial metrics with stock price volatility.
