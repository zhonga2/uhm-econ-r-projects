# Economic Research Project: Determinants of Hawaiʻi's Real GDP (2008–2025)

This project examines the relationship between Hawaiʻi’s **real GDP** and three major explanatory variables — **Brent crude oil prices**, **real visitor expenditures**, and **federal government obligations** — using quarterly data from 2008 Q1 to 2025 Q2.

---

## 📊 Overview

**Goal:**  
To identify which macroeconomic and policy-related factors most strongly influence Hawaiʻi’s real economic growth, using a log–log regression model estimated in R.

**Equation:**

$$\[
\log(\text{Hawaii Real GDP}) = \beta_0 - \beta_1 \log(\text{Brent Crude Price}) + \beta_2 \log(\text{Visitor Expenditures}) + \beta_3 \log(\text{Federal Obligations})
\]$$

---

## 🧠 Key Hypotheses

| Variable | Expected Sign | Rationale |
|-----------|----------------|------------|
| **Price of Brent Crude Oil** | Negative | Hawaiʻi’s energy system depends heavily on imported petroleum. Higher oil prices raise local energy and transportation costs, lowering real output. |
| **Total Real Visitor Expenditures** | Positive | Tourism is a core economic driver; reduced spending correlates with downturns such as during COVID-19. |
| **Federal Obligations** | Positive | Federal spending (especially defense) injects funds into the economy, stabilizing GDP growth. |

---

## 🧮 Data Sources

| Variable | Source | Frequency | Notes |
|-----------|---------|------------|--------|
| **Real GDP (HIRQGSP)** | U.S. Bureau of Economic Analysis / FRED | Quarterly | Millions of chained 2017 USD, seasonally adjusted. |
| **Brent Crude Price (POILBREUSDQ)** | International Monetary Fund / FRED | Quarterly | Proxy for Hawaiʻi’s energy import costs. |
| **Visitor Expenditures** | UHERO | Quarterly | Nominal data deflated using Honolulu CPI; 2020–2021 gaps handled with log-compatible constants. |
| **Federal Obligations** | USAspending.gov | Quarterly (derived) | Deflated using Honolulu CPI; includes defense and non-defense spending. |

---

## 🧰 Tools and Methods

- **Language:** R (RMarkdown `.Rmd`)
- **Libraries:** `ggplot2`, `dplyr`, `readr`, `tidyr`, `stats`
- **Techniques:**  
  - Log–log multiple linear regression  
  - Seasonal adjustment and CPI deflation  
  - Data cleaning of missing COVID-period values  
  - Visualization of correlations and residual diagnostics  

---

## 📈 Findings (Summary)

- **Brent Crude Price** → statistically significant **negative** relationship with GDP.  
- **Visitor Expenditures** → **positive**, strong elasticity.  
- **Federal Obligations** → **positive**, moderate elasticity, consistent with defense-driven spending patterns.  

These results support the hypothesis that Hawaiʻi’s GDP is most sensitive to tourism and federal spending, while oil prices act as a cost shock.

---

## 📚 References

- U.S. Bureau of Economic Analysis (2025). HIRQGSP Dataset. FRED, Federal Reserve Bank of St. Louis.  
- International Monetary Fund (2025). POILBREUSDQ Dataset. FRED, Federal Reserve Bank of St. Louis.  
- UHERO (2025). Total Real Visitor Expenditures.  
- USAspending.gov (2025). Federal Obligations for Hawaiʻi.  
- U.S. Energy Information Administration (2025). Hawaii State Energy Profile.  
- Hawaii Defense Economy (2023). Defense Spending Report.  

---

## 🧑‍💻 Author

**Anthony Zhong**  
B.A. Quantitative Economics | Minor in Information & Computer Sciences  
University of Hawaiʻi at Mānoa  

