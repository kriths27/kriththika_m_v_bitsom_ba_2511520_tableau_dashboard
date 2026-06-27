# Business Insights — Executive Dashboard
**Student:** Kriththika M V
**Dataset:** `dashboard_sales_data.xlsx` | **4,200 orders | Jan 2024 – Dec 2025**  
**Date:** 18 June 2026

---

> Each insight contains: **Observation → Data Evidence → Business Interpretation → Recommended Action**

---

## Insight 1 — Sales Trend: Consistent Growth with Seasonal Peaks

**Observation:**  
Monthly sales show an overall upward trajectory from January 2024 to December 2025, with clear peaks during certain months and a notable acceleration in the second half of each year.

**Data Evidence:**  
- Peak month reached ₹1.1Cr in sales (2025-08)
- Overall period total: **₹21.7Cr** across 4,200 orders
- 3-month moving average confirms sustained growth, not a one-off spike
- Year-on-year growth is visible across annual aggregation

**Business Interpretation:**  
The business is scaling. Seasonal peaks likely align with festive seasons (Q3-Q4 in India). The upward trend validates current growth strategy and marketing investments.

**Recommended Action:**  
Pre-stock inventory and increase marketing budgets 6 weeks before historically peak months. Build a seasonal demand forecasting model using this 2-year baseline. Don't over-interpret single-month dips — the trend is the signal.

---

## Insight 2 — Regional Performance: South Leads, East Lags

**Observation:**  
Regional performance is unequal, with South region generating the highest sales and East showing the lowest sales volume.

**Data Evidence:**  
- South: **₹6.5Cr** in total sales (1,210 orders)
- East: **₹4.9Cr** in total sales (897 orders)
- Profit margin variation across regions: 12.97% to 13.25%
- Return rates differ by region, indicating varying customer satisfaction levels

**Business Interpretation:**  
South region may have stronger distribution networks, higher urban density, or more effective regional sales teams. East may face infrastructure challenges or lower brand awareness.

**Recommended Action:**  
Investigate East's specific challenges (logistics, pricing, awareness). Deploy a regional growth pilot with dedicated account managers and targeted promotions. Replicate South's playbook where applicable.

---

## Insight 3 — Category Profitability: Technology Dominates, Furniture Under-Margins

**Observation:**  
While all three categories contribute to revenue, their profit margins differ significantly.

**Data Evidence:**  
- Technology: Margin = 17.64%, Sales = ₹15.4Cr
- Furniture: Margin = 5.82%, Sales = ₹5.2Cr
- Office Supplies: Margin = 14.39%, Sales = ₹1.1Cr
- 6.9% of all orders have negative profit — concentrated in high-discount Furniture

**Business Interpretation:**  
Technology products deliver the best return per rupee of revenue. Furniture likely suffers from high shipping costs and deep discount demands. Office Supplies have high volume but thin margins.

**Recommended Action:**  
Shift sales mix toward Technology. Review Furniture pricing strategy and cap discounts at 15%. For Office Supplies, focus on high-volume B2B corporate contracts to achieve scale economies.

---

## Insight 4 — Customer Segment: Corporate & Consumer Drive Revenue, Home Office Under-Penetrated

**Observation:**  
Three customer segments exist: Consumer, Corporate, and Home Office. Sales and profit concentration differs meaningfully across segments.

**Data Evidence:**  
- Corporate segment: 1,399 orders, avg rating = 4.07
- Consumer segment: 1,355 orders
- Home Office: 1,446 orders — smallest count
- Return rates vary by segment: Home Office = 5.67%

**Business Interpretation:**  
Corporate clients represent stable, large-order revenue. Home Office is under-served but growing post-pandemic — this is an emerging opportunity. Consumer segment is high-volume but lower average order value.

**Recommended Action:**  
Build a dedicated Home Office product bundle and campaign. Assign account managers to top 50 Corporate clients. For Consumer, focus on increasing basket size through cross-selling and loyalty programs.

---

## Insight 5 — Discount vs. Profit: Deep Discounts Destroy Margins

**Observation:**  
A clear negative correlation exists between discount rate and profit. Orders with discounts above 25% frequently generate negative profit.

**Data Evidence:**  
- Orders with discount > 25%: avg profit margin = **4.90%**
- Orders with discount ≤ 5%: avg profit margin = **18.28%**
- 592 orders (14.1% of total) have discounts > 25%
- Negative profit orders: 288 (6.9% of total)
- Trend line in scatter chart shows clear downward slope from discount to profit

**Business Interpretation:**  
Excessive discounting is actively destroying value. High discounts may be winning orders but at unsustainable economics. This is a commercial discipline problem that needs a policy fix.

**Recommended Action:**  
Implement a discount approval workflow: any discount > 15% requires manager approval, > 25% requires VP sign-off. Set category-level maximum discount caps. Retrain sales team on value-based selling.

---

## Insight 6 — Shipping Performance: Express Delivery Has Surprising Return Rate Pattern

**Observation:**  
Contrary to intuition, shipping speed does not linearly predict return rates. There are nuances by ship mode and delivery time bucket.

**Data Evidence:**  
- 0-1 day (Express): Return rate = 4.33%
- 6+ day (Slow): Return rate = 4.80%
- Avg delivery days by mode: Same Day=0.4d, First Class=1.8d
- Standard Class handles 2,435 orders (58.0% of total)

**Business Interpretation:**  
Express deliveries might serve urgent, high-expectation orders where quality issues are more visible. Slow deliveries may lead to order cancellations before delivery rather than returns. Standard Class is the workhorse of the operation.

**Recommended Action:**  
Investigate the return reason codes for express-delivered orders. Set a delivery SLA target of ≤ 4 days across all modes. Provide customers with real-time tracking to reduce "where is my order" support tickets.

---

## Insight 7 — Return Pattern: 4.5% Return Rate is Manageable but Regionally Uneven

**Observation:**  
The overall return rate of 4.55% is within industry norms, but regional and category-level variation creates specific risk areas.

**Data Evidence:**  
- Overall return rate: **4.55%** (191 returns out of 4,200 orders)
- Highest-returning category visible in return × category heatmap
- Regional return rate range: 4.34% to 4.91%
- Ship mode with highest return rate: First Class (5.08%)

**Business Interpretation:**  
Return concentration in specific regions may indicate product-market fit issues or logistics damage. Category-level returns for Furniture may relate to assembly difficulties or damage during shipping of large items.

**Recommended Action:**  
Implement a post-return survey to capture reason codes. Set a return rate reduction target of < 3% within 12 months. Prioritise quality control for high-return categories and packaging improvements for Furniture.

---

## Insight 8 — Risk & Opportunity: Campaign Channel Mix Needs Rebalancing

**Observation:**  
Sales are distributed unevenly across campaign channels, with some channels significantly outperforming others. This represents both a risk (over-dependence) and an opportunity (scalable channels are underutilised).

**Data Evidence:**  
- Top channel: **Organic** — ₹8.9Cr in sales (1,694 orders)
- Weakest channel: **Unknown** — ₹12.9L in sales
- Channel profitability varies: highest profit from Organic
- 24 orders (0.6%) have no campaign attribution — tracking gap

**Business Interpretation:**  
Over-reliance on a single channel is a business continuity risk. If the top channel experiences changes (algorithm shifts, cost increases), revenue could drop sharply. The attribution gap represents a significant measurement problem.

**Recommended Action:**  
Fix campaign attribution tracking immediately to eliminate the Unknown channel bucket. Run incremental channel experiments (20% budget test in underperforming channels). Target a more balanced 30/25/20/15/10% channel mix within 6 months to reduce concentration risk.
