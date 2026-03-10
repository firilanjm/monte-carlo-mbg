# Monte Carlo Simulation of Cash Waqf-Linked Sukuk (CWLS) for Sustainable MBG Funding

## Overview

This project evaluates the sustainability of the MBG (Makanan Bergizi Gratis) Fund using Monte Carlo simulations. Unlike traditional linear projections in Excel, this approach quantifies the probability of successfully funding a portion of the MBG program over a 10-year horizon under uncertain market yields and inflation. The MBG program is a government-run initiative in Indonesia aimed at ensuring access to nutritious meals for school-aged children.

The goal is to identify the “sweet spot” coverage — the maximum sustainable percentage of the MBG budget that can be funded with high confidence.

---

## Research Question

> *"With a yield of 6.4% and annual food inflation of 5%, what is the probability that the MBG Fund (Scenario B: Rp 200 trillion and Scenario C: Rp 400 trillion) can sustainably cover 2.5% and 5.0% respectively of the total MBG budget over the next 10 years?"*

Additional scenarios include:

- **Scenario A (Pesimis):** Rp 50 trillion principal  
- **Scenario B (Moderat):** Rp 200 trillion principal  
- **Scenario C (Optimis):** Rp 400 trillion principal  

---

## Methodology

- **Monte Carlo Simulation** in R  
- **Parameters:**
  - Yield CWLS Sukuk: 6.4% per year, volatility ±0.5%
  - MBG cost per meal: Rp 15,000
  - Beneficiaries: 20 million (Year 1) to 82.9 million (Year 5-10)
  - Inflation: 4–5% per year
- **Simulation Output:**
  - Coverage fraction per year and per simulation
  - Probability of sustaining a target coverage over 10 years
  - Distribution of coverage at year 10

- **Sweet Spot Analysis:**  
  For each probability threshold (50%, 80%, 90%, 95%, 99%), find the **maximum coverage fraction** that meets the sustainability criterion.

---

## Results

- **200T Principal:** Sweet spot coverage ≈ 2–2.5%  
- **400T Principal:** Sweet spot coverage ≈ 4–5%  
- **Coverage Trajectory:** Average coverage gradually decreases over the decade due to inflation and increasing beneficiaries.  
- **Year 10 Distribution:** Coverage exhibits variability, highlighting the importance of risk buffers.

---

## Visualizations

1. **Sweet Spot Plot** – maximum sustainable coverage vs probability threshold  
2. **Coverage Trajectory (Fan Plot)** – median coverage with 50% & 90% CI  
3. **Probability of Sustainability per Year** – bar chart of success probability  
4. **Year 10 Coverage Distribution** – density plot capturing variability  

Plots are saved using `ggsave()` and are publication-ready.

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/yourusername/mbg-fund-simulation.git
