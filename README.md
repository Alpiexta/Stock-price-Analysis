Stock Market Analysis and Predictions

📌 Project Overview
This project provides a comprehensive data science workflow for analyzing and predicting the performance of major technology stocks. Using historical data from the last three years, the analysis explores market trends, risk-reward profiles, and future price probabilities for a portfolio of industry leaders.

Stocks Analyzed
The project focuses on the Big Tech and semiconductor sectors, including:

1) AMD (AMD)
2) Nvidia (NVDA)
3) Apple (AAPL)
4) Google (GOOG)
5) Microsoft (MSFT)
6) Amazon (AMZN)
7) Tesla (TSLA)

🛠️ Tech Stack
Python: The core programming language.

yfinance: Used to fetch real-time and historical market data from Yahoo Finance.

Pandas & NumPy: For data manipulation and numerical analysis.

Matplotlib & Seaborn: For creating insightful visualizations and heatmaps.

📊 Analysis Breakdown
1. Data Retrieval and Preparation
We began by pulling three years of historical adjusted closing prices. This timeframe was chosen to capture various market cycles, including recovery periods and volatility, providing a robust dataset for analysis.

2. Moving Averages
Why we did it: Stock prices are inherently noisy. We calculated moving averages (e.g., 10-day, 20-day, and 50-day) to smooth out short-term fluctuations and identify the underlying trend direction.
Results: These plots help visualize "crossovers," where short-term trends break above or below long-term trends, often serving as indicators for market momentum.

3. Daily Returns and Risk Analysis
Why we did it: Understanding the daily percentage change is more critical for risk assessment than looking at price alone. We used histograms and KDE plots to visualize the distribution of these returns.
Results: The wider the distribution, the more volatile the stock. By comparing the "Expected Return" against the "Standard Deviation of Returns," we created a risk-return profile for each stock.

4. Correlation Analysis
Why we did it: To understand how these tech giants move in relation to one another, we generated a correlation heatmap.
Results: High correlation (close to 1.0) suggests that the stocks move in tandem, which is vital for portfolio diversification. The results typically show strong ties within the semiconductor industry (AMD and NVDA) and general software (MSFT and GOOG).

5. Monte Carlo Simulation (Predictive Modeling)
Why we did it: Since future stock prices are uncertain, we used a Monte Carlo simulation based on Geometric Brownian Motion (GBM). This method runs thousands of potential price paths based on historical volatility and drift.
Results: * Mean Final Price: Represents the average expected price after a set period (e.g., 365 days).

1% Quantile (Value at Risk): Shows a "worst-case" scenario, indicating the price point where there is only a 1% statistical probability of falling below.

Histogram of Simulations: Visualizes the probability distribution of final prices, helping to quantify the likelihood of reaching specific investment targets.