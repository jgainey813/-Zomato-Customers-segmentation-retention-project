# Zomato Customers — Segmentation & Retention (Tableau)

Interactive Tableau dashboard exploring **customer segments, RFM scores, and retention patterns** for Zomato-like food delivery data.

- **Live demo:** https://public.tableau.com/app/profile/joseph.gainey/viz/Book1_17512844917740/ZomatoCustomers?publish=yes
- **Tools:** Tableau (Public), SQL (optional), Excel/CSV
- **Role:** BI Analyst — data modeling, dashboard design, and storytelling

## Business Questions
1. Which customer segments (by **Recency, Frequency, Monetary**) drive the most orders and profit?
2. Where are churn risks highest and which cohorts are worth reactivation?
3. What targeted actions (offers, content, timing) will lift **repeat purchase rate** and **LTV**?

## Key Features
- **RFM segmentation** with clear segment labels (Champions, Loyal, Hibernating, At Risk)
- Cohort retention visualization (month-over-month repeat)
- Slice by **city, cuisine, device**, and date range
- KPIs: orders, AOV, repeat rate, revenue, CLV proxy

## Data
Use a sanitized/synthetic sample in `/data/` that mirrors these columns:

| column        | type   | example         |
|---------------|--------|-----------------|
| order_id      | string | 70012345        |
| order_date    | date   | 2024-05-16      |
| customer_id   | string | C-001234        |
| city          | string | Mumbai          |
| cuisine       | string | North Indian    |
| device        | string | iOS             |
| order_value   | number | 14.50           |

> Keep **PII out of Git**. Screenshots are fine; data is optional and synthetic only.

## How to Reproduce
1. Download/clone this repo
2. Open `tableau/ZomatoCustomers.twbx` (placeholder) and point to `/data/*.csv`
3. Publish to Tableau Public or Server

## Screenshots
Place exported PNGs from your Tableau viz here and reference them:

![RFM Overview](images/rfm-overview.png)
![Cohorts](images/cohorts.png)

## Metrics & Actions
- **RFM** buckets determine who to retain vs. reactivate
- **At-Risk** segment → email/SMS reactivation offer with decaying incentive
- **Hibernating** → low-cost nudge (free delivery off-peak), measure **repeat within 14 days**
- **Champions** → bundle/cross-sell premium cuisines

## Files
- `tableau/ZomatoCustomers.twbx` — packaged workbook (add yours)
- `images/` — screenshots exported from Tableau Public
- `docs/WRITEUP.md` — business summary & next steps
- `data/` — synthetic sample CSVs for reproducibility

---
### Attribution
Created by **J. Gainey** · TripleTen BIA · PTA/Dir. of Rehab → BI Analyst
