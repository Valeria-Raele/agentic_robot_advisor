
# Agentic Robo Advisor

## Personal Finance Management & Portfolio Optimization

An agent-based Robo Advisor designed to support personal financial decision-making, from budget monitoring and savings optimization to quantitative investment portfolio construction.

## Project Overview

The project aims to develop an intelligent virtual assistant capable of supporting users throughout the personal financial management cycle: from monitoring income and expenses to identifying savings opportunities and allocating available savings into an efficient investment portfolio.

The underlying objective is to connect two traditionally separate activities — **personal budget management and investment planning** — within a single analytical system. Rather than limiting the application to financial monitoring, the project extends its capabilities to support more complex decisions about how savings can be managed and invested.

The architecture is built on **LangGraph**, using a modular decision graph of specialized agents and tools. This approach allows the system to interpret natural-language requests, select the appropriate analytical task, execute financial calculations and generate structured responses. Context memory supports continuity across interactions.

### Interaction Flow

The system follows five main steps:

**1. User Input and Financial Data**

The assistant receives a dataset containing personal income and expense transactions. Users can submit natural-language questions about their financial position, including monthly balances, deficit categories, average savings and investment opportunities.

Historical financial market data are retrieved to support the investment analysis.

**2. Agent Decision and Task Selection**

A decision node interprets the user's request and selects the appropriate task within the LangGraph architecture.

Each task is associated with a specialized analytical component.

**3. Personal Finance Analysis**

The system performs three main activities:

- **Monthly cash flow analysis:** calculates income, expenses and monthly balances, identifying periods of financial deficit.
- **Expense analysis:** examines spending categories in months with negative balances, highlighting critical expenses and potential optimization opportunities.
- **Savings analysis:** estimates average monthly savings based on historical financial transactions.

These analyses establish the financial basis for subsequent investment planning.

**4. Investment Analysis and Efficient Portfolio Construction**

The investment component extends personal financial management into quantitative portfolio optimization.

The methodology follows two analytical stages.

**I. Financial Asset Analysis**

An initial selection of stocks and ETFs is organized across different investment categories, including safe-haven assets, technology, large-cap equities and global market indices.

Historical price distributions are examined, including excess kurtosis, to assess the characteristics of asset returns and the potential influence of extreme observations.

A **bootstrap methodology** is then applied by resampling historical daily returns to simulate potential future asset performance over a one-year horizon.

This approach incorporates the empirical characteristics of historical returns into the simulation process.

**II. Efficient Portfolio Optimization**

The portfolio construction process follows a mean-variance optimization framework.

Expected returns are estimated using historical average returns, while annualized volatility and the covariance matrix are calculated to assess individual asset risk and relationships between assets.

Monte Carlo simulations generate alternative portfolio allocations with different asset weights.

For each simulated portfolio, the system evaluates:

- Expected portfolio return.
- Annualized portfolio volatility.
- Covariance relationships between assets.
- Sharpe Ratio as a measure of risk-adjusted performance.

The portfolio with the **maximum Sharpe Ratio** is selected as the optimal allocation, identifying the combination of assets and percentage weights offering the most favorable risk-return balance under the model assumptions.

**5. Structured and Personalized Output**

The agent produces responses aligned with the user's request, combining quantitative results, financial interpretations and targeted suggestions.

The modular architecture also allows additional analytical tools and financial decision scenarios to be integrated progressively.

### Methodological Note on Expected Returns

Two distinct approaches are used for different analytical purposes:

- **Bootstrap simulations:** historical daily returns are resampled to estimate potential future asset performance while reflecting characteristics of their empirical distributions, including extreme observations and kurtosis.
- **Mean-variance portfolio optimization:** expected returns are estimated using historical average returns, consistently with the classical Markowitz framework, in which historical means and covariance relationships serve as inputs for portfolio construction.

### Conclusions

The project demonstrates how agent-based AI can support personal financial management across different levels of analytical complexity.

It combines relatively straightforward tasks, such as monitoring monthly cash flows and identifying savings opportunities, with more advanced quantitative activities involving financial market analysis, return simulations and portfolio optimization.

The resulting Robo Advisor provides a modular framework for connecting personal financial monitoring with structured, data-driven investment decision support.

## Personal Finance Management

- Analysis of income, expenses, savings and deficits.
- Identification of expense categories and opportunities for savings optimization.
- Conversational financial analysis using LangGraph agents and tools.

## Investment Portfolio Optimization

- Retrieval of historical stock and ETF market data.
- Analysis of return distributions and excess kurtosis.
- Bootstrap simulations of future asset prices and returns.
- Monte Carlo portfolio optimization using 5,000 simulated allocations.
- Evaluation of expected returns, annualized volatility and Sharpe Ratio.
- Agent-based integration of portfolio analysis and recommendations.

## Technologies

Python · Google Colab · LangGraph · LangChain · Pandas · NumPy · yfinance · SciPy · Matplotlib

## Project Files

- [AgenticAI_Personal_Finance_Management.ipynb](AgenticAI_Personal_Finance_Management.ipynb) — Main project notebook.
- [dataset/](dataset/) — Financial transactions dataset.

## Methodology

The system integrates personal budget analysis with market-based portfolio optimization through a modular agentic architecture, supporting progressive financial analysis and investment decision-making.

## Project Scope

Independent prototype developed for the application of agentic AI and quantitative methods to personal finance and portfolio management.
