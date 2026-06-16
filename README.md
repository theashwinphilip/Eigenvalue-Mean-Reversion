# Eigenvalue-Mean-Reversion
Eigenvector Mean-Reversion Strategy
Overview

This project implements a PCA-based statistical arbitrage strategy that identifies mean-reverting opportunities across a large equity universe using eigenvector decomposition of stock returns.

The strategy:

Collects and cleans historical stock price data.
Computes returns and covariance matrices.
Extracts latent factors using Principal Component Analysis (PCA).
Clusters stocks based on eigenvector loadings.
Removes common factor effects to isolate idiosyncratic residual returns.
Generates mean-reversion signals using rolling z-scores.
Constructs a market-neutral long/short portfolio.
Backtests performance with transaction costs and risk analytics.
Performs sensitivity testing and walk-forward validation.
Strategy Workflow
1. Data Ingestion
Downloads historical adjusted-close prices using Yahoo Finance.
Supports approximately 10 years of daily data.
Cleans missing values and removes invalid securities.
2. Return Computation
Computes daily log returns.
Performs exploratory data analysis (EDA).
Measures volatility and cross-sectional correlation.
3. Backtesting

Performance metrics include:

Annualized Return
Annualized Volatility
Sharpe Ratio
Sortino Ratio
Maximum Drawdown
Calmar Ratio
Alpha
Beta
Win Rate
4. Risk Analytics

Includes:

Value-at-Risk (VaR)
Conditional VaR (CVaR)
Drawdown analysis
Regime analysis (Bull/Bear/Sideways markets)
Return distribution diagnostics
5. Sensitivity Analysis

Tests robustness across:

PCA lookback windows
Number of factors
Entry/exit z-score thresholds
Portfolio size
6. Walk-Forward Validation

To reduce look-ahead bias:

Train PCA on historical windows.
Trade only on unseen future periods.
Aggregate out-of-sample performance across folds.
