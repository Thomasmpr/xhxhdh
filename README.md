# Portfolio Management Project – SEEGX Fund Analysis

## Project Overview

This project analyzes the **JPMorgan Large Cap Growth Fund (SEEGX)** and explores whether a portfolio built from its main holdings could outperform the fund itself.

The objective was twofold. First, we studied the characteristics and historical performance of the mutual fund. Second, we constructed an optimized portfolio using its largest holdings and compared both strategies from a risk-return perspective.

SEEGX is an actively managed **U.S. large-cap growth mutual fund** that invests mainly in companies with strong earnings growth potential. Because its investment strategy closely follows the growth segment of the U.S. equity market, the **Russell 1000 Growth Index** was used as the main benchmark. For additional comparison, we also included the **Russell 1000 Total Return Index** and the **MSCI World Index**.

The project therefore aims to answer a key portfolio management question:

> **Can a concentrated portfolio of a fund’s top holdings outperform the fund itself on a risk-adjusted basis?**

---

## Data Collection and Methodology

The empirical analysis was conducted using **Python**, primarily through the **yfinance** library to retrieve historical market data.

Daily price data for the selected securities were collected and then transformed into **monthly returns**. These returns were subsequently annualized in order to estimate key financial metrics such as:

- Expected returns  
- Variance and volatility  
- Covariance between assets  
- Portfolio risk and return characteristics  

The study covered the period **September 2020 to September 2025**, which allowed us to capture several important market phases, including:

- The **post-COVID market recovery**
- The **2022 inflation and interest rate shock**
- The **technology rally of 2023–2024**, partially driven by the boom in artificial intelligence

This timeframe provides a realistic environment to evaluate how growth stocks behave across different macroeconomic conditions.

---

## Portfolio Construction

The investment universe for the portfolio construction consisted of the **10 largest holdings of the SEEGX fund**:

**AAPL, AMZN, AVGO, GOOGL, MA, META, MSFT, NVDA, ORCL, TSLA**

Using these securities, we constructed an **efficient frontier** under standard portfolio constraints:

- Fully invested portfolio  
- Long-only positions  
- Optimization based on mean–variance theory  

From this efficient frontier, we selected a final **Effective Portfolio** using a **utility function** that reflects a specific level of investor risk aversion.

The resulting optimized portfolio concentrated its allocation into **six stocks**:

- AVGO  
- ORCL  
- GOOGL  
- MA  
- AAPL  
- NVDA  

The largest weights were assigned to:

- **AVGO – 48%**
- **ORCL – 20%**

These assets offered the most attractive contribution to return relative to risk and diversification benefits within the portfolio.

Stocks such as **AMZN, META, MSFT, and TSLA** were excluded from the final allocation because they did not improve the portfolio’s overall utility during the optimization process.

---

## Portfolio Performance

The optimized portfolio achieved:

- **Expected annual return:** ~36%  
- **Annual volatility:** ~25%

To evaluate its performance relative to the mutual fund and the benchmarks, several classical portfolio performance indicators were calculated:

- Standard Deviation  
- Sharpe Ratio  
- Beta  
- Jensen’s Alpha  
- Treynor Ratio  

The results reveal a clear trade-off between performance and risk.

The optimized portfolio generated a **Jensen’s Alpha of 18.51%**, suggesting strong stock-picking ability and significant excess returns relative to market risk.

However, this performance came with **substantially higher risk**, reflected in:

- **Beta: 1.237**
- **Volatility: 25%**

This indicates that the portfolio is significantly more sensitive to market movements and less diversified than the mutual fund.

---

## Comparison with the SEEGX Fund

Although the optimized portfolio generated higher raw returns and alpha, the **SEEGX mutual fund delivered better risk-adjusted performance**.

- **Sharpe Ratio (SEEGX): 1.45**
- **Sharpe Ratio (Optimized Portfolio): 1.27**

This means that per unit of risk taken, the mutual fund produced more stable and efficient returns. The main explanation lies in its **greater diversification**, which helps reduce volatility and smooth performance over time.

In contrast, the optimized portfolio behaves more like a **high-conviction strategy**, heavily exposed to a limited number of growth stocks.

---

## Key Takeaways

This project highlights an important principle in portfolio management.

A concentrated strategy can generate **significant excess returns** when stock selection is strong. However, insufficient diversification can dramatically increase portfolio risk and volatility.

In this case:

- The optimized portfolio represents a **high-risk, high-return strategy**.
- The SEEGX mutual fund represents a **more balanced and efficient investment solution** for most long-term investors.
