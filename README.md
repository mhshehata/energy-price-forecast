# German Electricity Price Forecasting — Portfolio Project

A data-driven analysis and forecasting model for German day-ahead electricity prices, 
built on real market data from the ENTSO-E Transparency Platform.

Built as a foundation for energy data consulting engagements in the DACH region.

---

## Project Status: Phase 1 — Exploratory Data Analysis ✅

---

## What This Project Does

Uses hourly German power market data to understand and forecast day-ahead electricity prices.
The analysis focuses on the relationship between renewable generation, system load, 
and price formation — the core mechanism driving European power markets.

---

## Key Findings So Far

**1. Renewables share is the dominant price driver (r = -0.80)**
As wind and solar generation increases as a share of total load, prices fall sharply.
This is the merit order effect — zero-marginal-cost renewables push expensive 
thermal plants off the margin.

**2. Intraday price structure mirrors the solar generation profile**
- Morning peak ~08:00: demand rises before solar kicks in
- Midday trough ~13:00: solar peaks, renewables share reaches 70%
- Evening peak ~19:00-20:00: solar gone, demand still high, prices spike to 3x midday levels

**3. Seasonal volatility is asymmetric**
- Winter: highest median prices, extreme upside spikes (up to 590 EUR/MWh)
- Spring: most negative price events — solar oversupply against collapsed heating demand
- Summer/Autumn: tighter distributions, more forecastable

---

## Data Sources

| Dataset | Source | Coverage |
|---|---|---|
| Day-ahead prices | ENTSO-E Transparency Platform | 2025, hourly, DE_LU bidding zone |
| Wind onshore generation | ENTSO-E Transparency Platform | 2025, hourly |
| Wind offshore generation | ENTSO-E Transparency Platform | 2025, hourly |
| Solar generation | ENTSO-E Transparency Platform | 2025, hourly |
| System load | ENTSO-E Transparency Platform | 2025, hourly |

---

## Tech Stack

- Python, Pandas, Matplotlib, Seaborn
- entsoe-py (ENTSO-E API client)
- JupyterLab
- Streamlit (dashboard — upcoming)

---

## Roadmap

- [x] Phase 1a: Pull and validate day-ahead price data
- [x] Phase 1b: Pull wind, solar, and load data
- [x] Phase 1c: Exploratory analysis — correlations, intraday and seasonal patterns
- [ ] Phase 2: Feature engineering and forecast model (linear regression → gradient boosting)
- [ ] Phase 3: Streamlit dashboard — interactive price forecast visualization
- [ ] Phase 4: First client engagement

---

## Author

Mohamed Shehata — Energy Data Analyst
Background: LNG operations, energy business engineering, MBA
Focus: Quantitative energy market analysis, DACH region

[GitHub](https://github.com/mhshehata) | [LinkedIn](#)
