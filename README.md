# Risk-Analysis-of-Tech-Stocks-Financial-Data

🧠 Project Overview (In Analytics Terms)
"Risk Analysis of Tech Stocks" is a data-driven exploration of financial market volatility among major tech companies. The notebook functions as a miniature quantitative risk assessment framework, leveraging time series analytics and descriptive statistics to understand each stock’s performance and relative risk. It mimics foundational components of financial analytics workflows often used by quants, analysts, and portfolio managers.

At its core, the project tackles questions like:

- How volatile are tech stocks individually and in relation to each other?

- What is the historical distribution of returns, and what can it tell us about future risk?

- How can simple statistical models inform investment decisions?

🧾 Dataset Description
The data used in this project is pulled dynamically from Yahoo Finance using the `yfinance` API, which fetches daily historical stock prices for selected companies.

Tech Stocks Analyzed:

- Apple Inc. (AAPL)

- Microsoft Corp. (MSFT)

- Amazon.com Inc. (AMZN)

- Alphabet Inc. (GOOGL)

- Meta Platforms Inc. (META)

Features Acquired:

- `Adj Close`: Adjusted closing price, used for return calculations

- `Date`: Timestamp field for time-series indexing

The data spans a multiyear horizon, giving room for insights across economic cycles and volatility periods.

📈 Analytical Methods & Techniques Used
1. Data Cleaning & Preparation
Time Series Structuring: Ensured datetime indexing and sorted chronologically.

DataFrame Harmonization: Combined individual stocks into a unified structure keyed by date.

2. Return Calculation
Daily Returns: Computed as:

Return𝑡 = (𝑃𝑡−𝑃𝑡−1) / 𝑃𝑡−1
where 𝑃𝑡 is the adjusted close price at time 𝑡.

3. Descriptive Statistics
-Mean Daily Return: Measures average return — proxy for expected return.

-Standard Deviation: Used as a volatility proxy.

-Rolling Volatility: 20-day window applied to smooth short-term variance trends.

-Correlation Matrix: Assesses interdependency between stock returns.

4. Risk Quantification
-Value at Risk (VaR) — Historical Simulation method:

  - Estimated at 95% and 99% confidence levels.
  
  - Highlights potential worst-case losses over a given period.
  
  - Particularly useful in portfolio-level analysis.

5. Visualization Tools using Matplotlib and Seaborn
- Line Charts: Track price movements and daily return trends.

- Histograms: Assess return distributions.

- Heatmaps: Display inter-stock correlations.

- Bar Plots: Compare returns and risk metrics.

🧠 Conceptual Framing
From a business intelligence lens, this project fits neatly within exploratory data analysis (EDA) and risk profiling. It primes the dataset for modeling and forecasting, such as:

-Portfolio optimization

-Monte Carlo simulations

-Beta/Sharpe ratio computation
