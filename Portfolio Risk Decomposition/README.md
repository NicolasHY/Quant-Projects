# Quant-Projects

Personal quantitative finance projects exploring factor models, portfolio construction, and risk analytics. Built alongside my M2 in Financial Markets & Investments at SKEMA Business School and independent study of Paleologo's *Advanced Portfolio Management*.

### Portfolio Risk Analytics
End-to-end factor risk framework on the 30 most liquid S&P 500 names (2015–2024).

- Factor model: Fama-French 3-factor decomposition with HAC-robust OLS and rolling betas
- Risk decomposition: systematic vs idiosyncratic split; factor-level contribution analysis
- VaR / CVaR: historical, parametric (normal and Student-t), stressed VaR on the COVID window
- Backtesting: Kupiec Proportion of Failures test across all VaR models
- Stress testing: forward-looking factor shock scenarios (GFC replay, rates shock, flight to quality)
- Optimization: minimum-variance overlay in cvxpy with tracking error and factor-tilt constraints

Key finding: parametric normal VaR fails Kupiec at 99% with roughly 2x the expected violation rate; Student-t(5) improves but still rejects, pointing to volatility clustering that a static parametric model cannot capture.

## Stack

Python, NumPy, pandas, statsmodels, cvxpy, yfinance, matplotlib, plotly.

## About

Nicolas Henry. M2 Financial Markets & Investments