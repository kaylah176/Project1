# Project1 : Pre and Post-midterm Election Stock Market Performance


Our project focuses on optimizing portfolio performance by analyzing six industries' performance the past ten years, over the last five midterm - elections. <br>
We aim to validate trends in our data based on the political and economic climate during this period. <br>
This analysis will provide investors with insights on portfolio positioning to safeguard their investments. <br>
Additionally, we will emphasize geographic data to visualize regions with political party affiliation and cross-reference them with relevant industries.<br>
___
## Technologies
- The **Investment Insights: Industry Trends in Political Climates** is written in Python.<br>
- Visualizations are generated using the hvPlot and Matplotlib libraries.<br>
___
## Installation Guide
- Transfer the repository contents to the designated folder on the user's computer, ensuring the preservation of the directory structure.
- The application was created using Python version 3.11.7. <br>
  To run the application on your local machine, ensure the installation of the following Python packages:<br>

- Pandas <br>
- Matplotlib <br>
- Yahoo_fin<br>
- HvPlot <br>
- Jupyterlab<br>

These packages can be installed  individually into the preferred environment.

`pip install pandas`
`pip install matplotlib`
`pip install hvplot`
`pip install jupyterlab`
`pip install yfinance`
___
## 1. Initial Data 
  - Through a market research, we chose the top 6 industries (Technology, Healthcare, Financial, Consumer Discretionary, Energy, and Weapons Manufacturing) and 3 stocks of each.
  - Defined stock ticker and date range, and dowloaded the data from Yahoo Finance.
  -  Gather data on the outcomes of the Senate and House of Representatives elections for the last 5 elections.

 ___ 
## 2. Creating a Database of Each Stock
   - Created a DataFrame of the closing prices and dates of each stock per industry <br>
  - Combined all stocks from the 6 industries into a single DataFrame: `custom_portfolio_df`
  - Assigned the close column to a new DataFrame :`small_df`
  - Used the `.columns` attribute to assign new column names to the DataFrame `small_df` 
  - Created a new DataFrame that includes only columns correspondent ton the stock of each industry :
  `tech_df = small_df[['AAPL', 'MSFT', 'GOOG']]`
  `health_df=small_df[['JNJ','PFE','UNH']]`
  `finance_df=small_df[['JPM','BAC','V']]`
  `consumer_df=small_df[['AMZN','NKE','DIS']]`
  `energy_df=small_df[['XOM','FSLR','NEE']]`
  `weapons_df=small_df[['LMT','RTX','NOC']]`
___
## 3. Calculate Daily Returns and Weighted Returns 
- Calculated Daily Returns of each industry in order to do a performance comparison
  `tech_daily`
  `health_daily`
  `finance_daily`
  `consumer_daily`
  `energy_daily`
  `weapons_daily`
- Dropped Nulls<br>
- Generated a combined Daily Returns DataFrame<br>
- Renamed each column with the ticker' name <br>
- Set weights <br>
- Created an empty dictonary to store the returns of each sector <br>
___
## 4. Risk Analysis Performance 
**- Cumulative returns of Each Industry** <br>

- Collect cumulative returns for each industry for 1 year before and 1 year after each midterm election.<br>

![alt text](IMAGES/CUMULATIVE_RETURNS_10%20YEARS.png)

**- Annualized Standard Deviation** <br>
 

![alt text](IMAGES/STANDARD_DEVIATION.png)

**- Annualized Sharpe Ratios**<br>
-  Compute the Sharpe ratio for each industry using the cumulative returns<br>
-  The Sharpe ratio measures the risk-adjusted return of an investment. It's calculated as the average return minus the risk-free rate, divided by the standard deviation of returns<br>

- The proximity to zero, as indicated by the 0.54 value, suggests a moderate level of risk-adjusted return within the Tech industry, indicating a comparatively lower investment risk.<br>

![alt text](IMAGES/SHARPE_RATIOS.png)

___
## 5. Statistical Analysis
  
- Analysed the  performance of each industry during time frame - 1 year before midtern, 1 year after midterm -- do this for 5 different terms <br>
- Calculate the average growth of each industry<br>
- Top performing industries get put into a portfolio weighted accordingly<br>
- Why does the market underperform in the 12 months leading up to midterm elections and over-perform the 12 months after midterm elections?<br>
- What variables lead to the underperformance and over-performance in the midterm elections? <br>

## 5.1. 
- Analyze Performance based on Election Outcomes.<br>
- Group the election outcomes by party (e.g., Republican or Democrat).<br>
-  Calculate the average cumulative returns for each industry for periods following elections when each party won control of the Senate and the House of Representatives.<br>
-  Compare the average cumulative returns across industries for each party's control.<br>

**Midterm 1:**
12 Months Before 
2013-11-01 to 2014-10-31
 12 Months After 
2014-11-01 to 2015-10-31

**Midterm 2:**
 12 Months Before 
2015-11-01 to 2016-10-31 
 12 Months After 
2016-11-01 to 2017-10-31

**Midterm 3:**
12 Months Before 
2017-11-01 to 2018-10-31
 12 Month After 
2018-11-01 to 2019-10-31

**Midterm 4:**
12 Months Before 
2019-11-01 to 2020-10-31
 12 Months After 
 COVID SO THIS IS AN ANOMALY: 2020-11-01 to 2021-10-31

 **Midterm 5:**
12 months Before 
2021-11-01 to 2022-10-31
12 Months After 
2022-11-01 to 2023-10-31

**Upcoming Election that hasn't occurred yet: 12 Months Before**
- Predictions on how well our portfolio will do before the next midterm election 
2023-11-01 to 2024-10-31
- Forecasting: We would want to predict which industry would potentially do the best in the next primary election based on what party gets elected 
___
## 6. Data Visualization 
  

- Determine which industries performed best and were safest under different election outcomes <br>
- Analyzed which party was in power after each major election<br>
- Consider any trends or patterns that emerge from your analysis<br>
-  Identify any industries that consistently perform well or poorly regardless of election outcomes<br>
- Created our own ideal portfolio that only include the industries that performed the best for the last 5 elections<br>
- Averaged the cumulative returns (include points where the party in power changes) of each industry and find the highest<br>
- Included the top 3 industries.
  
**Monte Carlo Simulation: Now until 2024-11-01**

Statistical Analysis on the portfolio: Volatility (interact hvplot), Cumulative Returns plot
Data Visualization: Results of all the past 5 midterm elections
Weights:
___
## 7. Contribuitors
[Heloísa Bonetti](https://github.com/helobonetti)<br>
[Kayla Hofmann](https://github.com/kaylah176)<br>
[Krish Nair](https://github.com/krishn100)<br>
___
## 8. Findings

___
## 9. Future Work
Prospective developments or improvements to this project encompass:<br>
- Execute a more comprehensive risk analysis questionnaire<br>
- Integrate the Russia-Ukraine conflict into the analysis<br>
-  How would the **Consumer Price Index (CPI**) be affected before and after the last 5 midterm elections in the US ?<br>
- Incorporate functionalities that enable users to fine-tune their portfolios<br>
- Enhance the quality of visual representations<br>

## 10. How to Run the Code

- Clone the repository and execute it from the notebook in chronological order of the midterm dates <br>
- The 'image' folder must be established in the environment; otherwise, an error will occur.


  





