CAPM Calculation – Python Exercise\
Overview:
- This project demonstrates the calculation of a stock’s expected return using the Capital Asset Pricing Model (CAPM).
- We process historical stock and market return data, compute Beta, and apply the CAPM formula with a given risk-free rate to estimate the expected return.

Data Inputs:
- File Name: data.csv
- Data Extracted from https://dps.psx.com.pk/historical
- We have taken HBL (stock data) and KSE-100 Index (market index data) for the year 2021 (12 months)
- Trading Days = 246
- Columns Required:
- DATE – Date of the observation
- Return_Stock – Stock’s daily returns (as decimals, e.g., 0.005 for 0.5%)
- Return_Market – Market index daily returns (as decimals)
- Risk-Free Rate (Rf): Given as 10.095% (annualized), 10-Year Bond Yield in 2021

Steps Performed:
1. Import Libraries:
- We use pandas for data handling and numpy for numerical operations.
2. Load the Dataset
3. Data Cleaning:
- Removed unused columns (e.g., empty Risk-Free Rate column that had only NaN values).
- Verified no missing values in Return_Stock or Return_Market.
4. Calculate Average Market Return
5. Calculate Beta (β)
6. Apply CAPM Formula: Expected Return=Rf + β×(Rm −Rf)\
  Where:\
  𝑅𝑓  = Risk-Free Rate = 10.095% = 0.10095\
  𝑅𝑚  = Average Market Return = 0.00006 (0.006%)\
  𝛽 = 0.8747
7. Final Output:\
  Risk-Free Rate: 10.095%\
  Average Market Return: 0.006%\
  Beta: 0.8747\
  CAPM Expected Return: 1.270%
  
Key Insights:
- Low average market return resulted in a significantly lower CAPM expected return than the risk-free rate, indicating the market underperformed relative to the fixed return benchmark.
- Beta < 1 shows the stock is less volatile than the market.


