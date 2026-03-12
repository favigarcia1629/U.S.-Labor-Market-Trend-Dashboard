# U.S. Labor Market Trend Dashboard 📊
**Portfolio Project #02 | EDA & Visualization | Python | BLS API**

## Results at a Glance

| Coverage | Indicators Tracked | Data Source | Time Span |
|----------|--------------------|-------------|-----------|
| U.S. National | Unemployment, Wages, Job Openings | Bureau of Labor Statistics | 1990 – 2025 |

> Visualized the fastest labor market collapse in U.S. history — unemployment jumped from **3.5% to 14.7% in 8 weeks** during the COVID-19 shock of 2020.

---

## Overview

This project retrieves and visualizes U.S. labor market data from the Bureau of Labor Statistics (BLS) public API, covering unemployment rates, wage growth, and job openings across 35 years. Each chart is annotated with key economic events to tell the story of the American labor market through data.

The dashboard demonstrates that visualizing economic data is not just a technical skill — it is a **policy communication** skill. The Fed, Congressional Budget Office, and IMF all rely on dashboards like this to brief decision makers.

---

## Dataset

**Source:** Bureau of Labor Statistics (BLS) Public API — free, no account required

| Series | BLS Code | Economic Meaning |
|--------|----------|-----------------|
| Unemployment Rate (U-3) | LNS14000000 | Standard measure — actively seeking work |
| U-6 Unemployment | LNS13327709 | Broader measure including discouraged workers |
| Average Hourly Wages | CES0000000008 | Key inflation signal — above 3–4% signals pressure |
| Job Openings (JOLTS) | JTS000000000000000JOL | Leading indicator of labor demand |
| Labor Force Participation | LNS11300000 | More complete picture than unemployment rate alone |

---

## Methodology

**1. API Data Retrieval**
Automated data pull from BLS API with error handling. All series retrieved programmatically — no manual downloads.

**2. Time Series Cleaning**
Seasonal adjustment verified. Missing values handled via forward-fill for alignment consistency.

**3. Multi-Panel Visualization**
Multi-panel Matplotlib dashboard with annotated event markers for 2001, 2008, 2020, and 2022 recessions and shocks.

**4. Economic Storytelling**
Each panel designed to communicate a specific policy-relevant insight rather than just display raw data.

---

## Key Findings

- **The 2020 COVID shock was unlike any prior recession** — unemployment spiked 11 percentage points in 8 weeks, compared to 5 points over 18 months in 2008
- **Wage growth above 3–4% reliably preceded inflation surges** — visible in the 2021–2023 data, consistent with wage-push inflation theory
- **Job openings (JOLTS) peaked before unemployment reached its low** — confirming JOLTS as a leading, not coincident, labor market indicator
- **U-6 consistently ran 1.7–2x higher than U-3** — standard unemployment statistics systematically undercount labor market slack

---

## How to Run

Requires a free BLS API key from [bls.gov/developers](https://www.bls.gov/developers/)

```bash
pip install pandas matplotlib seaborn requests
# Add your BLS API key to the config cell in the notebook
jupyter notebook labor_market_dashboard.ipynb
```

---

## Tools & Libraries

- Python 3.12
- `requests` — BLS API calls
- `pandas` — time series manipulation
- `matplotlib` / `seaborn` — multi-panel dashboard

---

## About

Built as part of an Economics portfolio by an economics major exploring machine learning applications in finance and policy.
