# NSE Alpha Screener & Portfolio Simulator

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![NSE](https://img.shields.io/badge/Market-Nairobi%20Securities%20Exchange-003087?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## Project Overview

A **professional-grade Excel workbook** that screens all major stocks listed
on the **Nairobi Securities Exchange (NSE)** using a custom 5-factor weighted
scoring model — and simulates portfolio performance with real capital allocation.

This project was built to demonstrate that **capital markets analytics**
does not require expensive Bloomberg terminals or Python scripts.
A well-structured Excel model can deliver institutional-quality
stock screening for any East African investor or analyst.

> Data as at: December 2024
> ,Simulated Capital: KES 100,000
> , Universe: 25 NSE-listed companies across 6 sectors

---

## Problem Statement

Retail investors and junior analysts in Kenya lack accessible tools to:

- Objectively compare NSE stocks across multiple financial factors
- Understand which sectors offer the best risk-adjusted returns
- Simulate portfolio construction before committing real capital

This workbook solves all three problems in one file.

---

## The Scoring Model

Each stock is scored out of **100** using 5 financial factors:

| Factor      | Metric                 | Weight | Logic                            |
| ----------- | ---------------------- | ------ | -------------------------------- |
| Valuation   | P/E Ratio              | 25%    | Lower P/E = higher score         |
| Income      | Dividend Yield (%)     | 20%    | Higher yield = higher score      |
| Growth      | EPS Growth YoY (%)     | 20%    | Higher growth = higher score     |
| Asset Value | P/B Ratio              | 20%    | Lower P/B = higher score         |
| Momentum    | 52-Week Price Recovery | 15%    | Stronger recovery = higher score |

**Scoring Method:** PERCENTRANK normalization ensures every stock
is fairly compared relative to the full universe — not on absolute numbers.

**Rating Scale:**

| Score | Rating       |
| ----- | ------------ |
| ≥ 75  | Strong Buy   |
| 60–74 | Buy          |
| 45–59 | Hold         |
| 30–44 | Underperform |
| < 30  | Avoid        |

---

## Workbook Structure

| Sheet             | Purpose                                                        |
| ----------------- | -------------------------------------------------------------- |
| `Stock_Data`      | Raw fundamentals for 25 NSE stocks across 6 sectors            |
| `Screener`        | 5-factor scoring engine — ranks every stock out of 100         |
| `Portfolio_Sim`   | Capital allocator — pick stocks, invest capital, see returns   |
| `Sector_Analysis` | Sector-level averages, best stock per sector, charts           |
| `Dashboard`       | Executive KPI dashboard — top picks, charts, portfolio verdict |
| `Assumptions`     | Model weights, data sources, methodology documentation         |

---

## Key Features

- **Automated stock ranking** — composite score updates instantly when data changes
- **Interactive portfolio builder** — dropdown stock selection, capital allocation
- **Sector intelligence** — AVERAGEIF aggregations across 6 NSE sectors
- **Benchmark comparison** — portfolio return vs Kenya T-Bill rate
- **Traffic-light formatting** — color-coded scores, ratings and risk indicators
- **Dynamic dashboard** — KPI cards, top 5 table, sector donut chart
- **Dividend income tracking** — annual dividend projected from shares held

---

## Stock Universe (25 Companies)

| Sector            | Companies                                                    |
| ----------------- | ------------------------------------------------------------ |
| **Banking**       | Equity Group, KCB, Co-op Bank, NCBA, DTB, Stanbic, StanChart |
| **Telco**         | Safaricom                                                    |
| **Insurance**     | Jubilee, Britam, CIC, Kenya Re                               |
| **Manufacturing** | EABL, BAT Kenya, Unga Group, Crown Paints, Bamburi           |
| **Energy**        | TotalEnergies Kenya, KenolKobil, Kenya Power, Umeme          |
| **Investment**    | Centum, I&M Holdings, Olympia Capital, Nation Media          |

---

## Excel Skills Demonstrated

```
- Cross-sheet formulas        - PERCENTRANK & RANK
- VLOOKUP & INDEX-MATCH       - IFS & IFERROR
- COUNTIF & AVERAGEIF         - MAXIFS & LARGE
- Data Validation dropdowns   - Conditional Formatting
- Color Scales & Icon Sets    - Pie & Bar Charts
- KPI Card design             - Freeze Panes & Print Layout
```

---

## Screenshots

### Executive Dashboard_1

![Dashboard](screenshots/05_dashboard_1.png)

### Executive Dashboard_2

![Dashboard](screenshots/05_dashboard_2.png)

### Stock Screener — Scoring Engine

![Screener](screenshots/02_screener.png)

### Portfolio Simulator

![Portfolio](screenshots/03_portfolio_sim.png)

### Sector Analysis

![Sector](screenshots/04_sector_analysis.png)

### Assumptions

![Assumptions](screenshots/06_assumptions.png)

---

## Repository Structure

```
 NSE-Alpha-Screener/
│
├──  NSE_Alpha_Screener_Dec2024.xlsx
├──  README.md
└──  screenshots/
    ├── 01_dashboard.png
    ├── 02_screener.png
    ├── 03_portfolio_sim.png
    └── 04_sector_analysis.png
```

---

## How to Use

1. **Download** the `.xlsx` file from this repository
2. Open in **Microsoft Excel** (2016 or later recommended)
3. Go to **`Stock_Data`** sheet to review or update stock fundamentals
4. Go to **`Screener`** to see the auto-ranked stock scores
5. Go to **`Portfolio_Sim`** — use the dropdowns in column B to pick stocks
6. Type your investment amount in the **Amount Invested** column
7. Watch the **Dashboard** update automatically with your portfolio stats

---

## How to Customize

- **Update prices** in `Stock_Data` → all scores recalculate automatically
- **Adjust scoring weights** in the `Assumptions` sheet
- **Change starting capital** in the Portfolio_Sim settings panel
- **Add new stocks** by inserting rows in `Stock_Data` and extending formula ranges

---

## Data Sources

| Source                                           | Usage                             |
| ------------------------------------------------ | --------------------------------- |
| [Nairobi Securities Exchange](https://nse.co.ke) | Share prices, P/E ratios          |
| [Investing.com](https://investing.com)           | Historical prices, EPS, dividends |
| [African Markets](https://african-markets.com)   | Cross-reference fundamentals      |

---

## Disclaimer

This workbook is built for **educational and portfolio demonstration purposes only**.
It does not constitute financial advice. Always conduct your own research
before making investment decisions. Data is as at December 2024.

---

## Author

**[Stephen Maina]**
Data Analyst in | Excel • SQL • Python • Power BI

[![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?style=flat&logo=github)](https://github.com/yourusername)

---

_If you found this project useful, please give it a star!_
