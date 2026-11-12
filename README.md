
# Agentic Robo Advisor

## Personal Finance Management & Portfolio Optimization

An agent-based Robo Advisor designed to support personal financial decision-making, from budget monitoring and savings optimization to quantitative investment portfolio construction.

## Project Overview

### Objective: Integrated Personal Budget and Savings Management

The project aims to develop an intelligent virtual assistant for the **integrated management and optimization of personal finances**, supporting the user throughout the entire financial management cycle: from monitoring income and expenses to identifying budget imbalances, improving spending efficiency, assessing savings capacity, and allocating available savings into an efficient investment portfolio.

The central objective is to **optimize both sides of personal financial management**:

- **Expense management:** identify the spending categories responsible for negative monthly balances, understand their contribution to financial deficits, and highlight opportunities to improve budget efficiency.
- **Savings and investment management:** assess the financial resources available for saving and investment, monitor the personal financial reserve, and support the allocation of investable savings into a diversified portfolio of financial assets, selected through quantitative risk-return analysis.

The project therefore connects **personal budget analysis with investment portfolio optimization**, treating investment decisions as part of a broader financial planning process rather than as an isolated market analysis.

The architecture is based on **LangGraph**, which organizes specialized agents and analytical tools into a modular decision graph. Natural-language processing enables the assistant to interpret user requests, select the appropriate financial analysis, and generate structured responses, while conversational memory supports continuity across interactions.

### Interaction Flow and Analytical Methodology

**I. Personal Financial Data and User Requests**

The assistant receives a dataset containing personal income and expense transactions.

Users can ask questions such as:

- What are my monthly income, expenses, and financial balances?
- Which spending categories contribute most to my monthly deficits?
- Where can I optimize my expenses?
- How much can I save on average each month?
- How can I allocate my savings into an efficient investment portfolio?

The system combines personal financial data with updated financial market data to address both budget management and investment planning.

**I.I. Agent Decision and Task Selection**

A decision node interprets each natural-language request and selects the most appropriate task within the LangGraph architecture.

Specialized analytical tools perform the required calculations and return results for the agent to interpret and communicate.

**I.II. Personal Budget Monitoring and Expense Optimization**

The first analytical component focuses on understanding and improving the user's financial position.

It performs three principal tasks:

- **Monthly cash flow analysis:** calculates income, expenses, and net monthly balances, identifying periods of surplus and deficit.
- **Expense analysis in deficit months:** examines the spending categories contributing to negative balances, identifies the most critical expense items, and highlights potential areas for cost optimization.
- **Savings capacity analysis:** estimates average monthly savings from historical income and expense patterns, providing a quantitative basis for assessing the resources potentially available for investment.

These activities establish the connection between **spending optimization, savings generation, and the management of the personal financial reserve**.

The purpose is not simply to report financial transactions, but to identify where financial resources can be managed more efficiently and how the resulting savings can support longer-term investment decisions.

**I.III. Savings Allocation and Quantitative Investment Analysis**

The second analytical component focuses on the efficient allocation of savings into a portfolio of stocks and ETFs.

The investment process is developed through two successive analytical stages.

**I.IV. Financial Asset Analysis and Return Simulation**

The analysis begins with a selection of financial assets organized into different investment categories, including safe-haven assets, technology stocks, large-cap equities, and global market indices.

Historical financial market data are retrieved and analyzed to examine the behavior and distribution of asset returns.

Particular attention is given to **kurtosis**, which helps identify distributions characterized by extreme observations and tail risk.

The **bootstrap technique** is then applied to historical daily returns, generating simulated return scenarios through repeated sampling of the observed return distribution.

This methodology is used to estimate potential future asset performance over a one-year horizon while accounting for the empirical characteristics of historical returns.

The analysis provides an initial assessment of individual asset behavior before portfolio construction.

**II. Efficient Portfolio Construction and Monte Carlo Optimization**

The next stage aims to identify an efficient allocation of available savings among the selected financial assets.

The portfolio optimization framework incorporates:

- **Expected returns:** estimated from historical average asset returns.
- **Annualized volatility:** used to measure the variability and risk of individual asset returns.
- **Covariance matrix:** used to evaluate relationships between assets and the effects of their combined risk within a portfolio.
- **Portfolio weights:** representing the percentage allocation of invested capital across the selected assets.
- **Sharpe Ratio:** used to evaluate portfolio performance relative to the level of risk assumed.

A **Monte Carlo simulation** generates thousands of alternative portfolios with different combinations of asset weights.

For each simulated portfolio, expected return, volatility, and the Sharpe Ratio are calculated.

The allocation that achieves the **maximum Sharpe Ratio** is selected as the optimal portfolio under the model assumptions, identifying the combination of financial assets and percentage weights offering the most favorable risk-adjusted expected performance.

This process connects the management of personal savings with quantitative investment decisions, providing a structured approach to the allocation of investable financial resources.

**II.I. Structured Financial Assessment and Personalized Output**

The agent integrates the results of the relevant analytical tasks and provides responses consistent with the user's request.

Outputs may include:

- Monthly budget summaries and cash flow assessments.
- Identification of deficit periods and critical expense categories.
- Savings capacity estimates and opportunities for spending optimization.
- Quantitative analysis of financial assets and simulated returns.
- Portfolio allocations, expected performance, volatility, and risk-adjusted evaluation.

The resulting system supports a progression from **financial monitoring to expense optimization, savings assessment, and investment portfolio construction**.

### Methodological Note on Expected Returns

Two distinct approaches are used for different analytical purposes:

- **Bootstrap simulations:** historical daily returns are resampled to estimate potential future asset performance while reflecting characteristics of their empirical distributions, including extreme observations and kurtosis.
- **Mean-variance portfolio optimization:** expected returns are estimated using historical average returns, consistently with the classical Markowitz framework, in which historical means and covariance relationships serve as inputs for portfolio construction.

### Conclusions

The project demonstrates how **agent-based AI can support the integrated management of personal finances**, combining the optimization of expenditure with the efficient allocation of savings.

Its distinctive feature is the connection between two complementary financial decisions: **how to improve the personal budget and how to invest the financial resources available after assessing income, expenses, savings capacity, and financial reserves**.

The assistant supports both straightforward financial monitoring activities and more complex quantitative investment analyses, incorporating historical return distributions, kurtosis, bootstrap simulations, covariance analysis, Monte Carlo portfolio optimization, and Sharpe Ratio maximization.

The resulting Robo Advisor provides a modular, data-driven framework for personal financial decision support, linking everyday budget management with structured investment planning.

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

Independent prototype developed for the application of agentic AI and quantitative methods to personal finance and portfolio management.
