# Chart Selection Justification
**Student:** Kriththika M V  
**Dashboard:** Executive Sales Performance Dashboard

Each chart is justified below using: Question Answered | Chart Type Rationale | Fields Used | Design Principle | Mistake Avoided.

---

## Chart 1 — Monthly Sales & Profit Trend (Line Chart with Dual Axis)

| Attribute | Detail |
|---|---|
| **Question Answered** | How have sales and profit evolved month-over-month over 24 months? Is growth sustained or volatile? |
| **Why Line Chart** | Line charts are optimal for time-series data — they visually encode temporal continuity and make trend direction immediately obvious. Area fill reinforces magnitude. |
| **Fields Used** | X-axis: `order_year_month` (time), Y-axis: `total_sales` (primary), Secondary Y: `total_profit` / `profit_margin` |
| **Color/Mark** | Sales = Cyan (accent1), Profit = Green (accent3), Moving Average = Amber (accent5) |
| **Design Principle** | Dual Y-axis allows simultaneous comparison of volume (sales) and efficiency (margin). 3-month moving average reduces noise and reveals the underlying trend. |
| **Mistake Avoided** | Did NOT start Y-axis at zero for the line — doing so would compress variance. Did NOT use bar chart for time-series as it hides continuity. |

---

## Chart 2 — Regional Sales & Profit (Grouped Bar Chart)

| Attribute | Detail |
|---|---|
| **Question Answered** | Which regions generate the most revenue? How does regional profit compare to sales? |
| **Why Grouped Bar** | Grouped bars allow direct comparison of two related metrics (Sales vs. Profit) across discrete categories (Regions). The grouping makes the margin gap visually apparent. |
| **Fields Used** | X-axis: `region`, Y-axis: `total_sales` and `total_profit` (grouped), Color: Region-specific palette |
| **Design Principle** | Sort regions by descending sales to draw attention to top/bottom performers immediately. |
| **Mistake Avoided** | Did NOT use pie chart — it would hide the magnitude differences between regions. Avoided 3D bars which distort visual perception. |

---

## Chart 3 — Category Profitability (Bar Chart + Gauge)

| Attribute | Detail |
|---|---|
| **Question Answered** | Which product category is most profitable? What is each category's profit margin? |
| **Why Bar + Gauge** | Bar chart gives absolute profit comparison; gauge chart communicates margin % as a proportional fill — both are needed for a complete picture of category health. |
| **Fields Used** | Category (X), total_profit (Y), profit_margin (gauge fill) = `profit / sales` (calculated field) |
| **Color** | Consistent category colours throughout dashboard (Furniture=Cyan, Office=Purple, Tech=Green) |
| **Design Principle** | Semantic colour consistency — same category always maps to same colour across all charts. |
| **Mistake Avoided** | Did NOT show margin only — a high margin on a tiny revenue base is misleading. Showing both profit and margin together avoids this. |

---

## Chart 4 — Customer Segment Mix (Donut Chart)

| Attribute | Detail |
|---|---|
| **Question Answered** | What proportion of sales comes from each customer segment? Is the business over-reliant on one segment? |
| **Why Donut Chart** | Donut charts communicate part-to-whole relationships clearly. The hollow centre allows for a summary annotation (segment count). Better than a full pie as it de-emphasises the wedge area encoding which can mislead. |
| **Fields Used** | `customer_segment` (category), `total_sales` (size of wedge) |
| **Color** | Cyan (Consumer), Purple (Corporate), Green (Home Office) — distinct, non-adjacent in spectrum |
| **Design Principle** | Limited to 3 segments — donut charts lose effectiveness beyond 5 segments. |
| **Mistake Avoided** | Did NOT use a 3D pie chart. Did NOT have too many slices. Did NOT show percentages without labels. |

---

## Chart 5 — Shipping Mode Performance (Horizontal Bar)

| Attribute | Detail |
|---|---|
| **Question Answered** | How long does each shipping mode take to deliver? Which mode is fastest/slowest? |
| **Why Horizontal Bar** | Horizontal bars work better than vertical when category labels are multi-word (e.g., "Standard Class", "Same Day"). Label readability is preserved without rotation. |
| **Fields Used** | `ship_mode` (Y-axis), `avg_delivery_days` = average of `delivery_days` (X-axis) |
| **Color** | Colour-coded by mode; consistent with shipping-related chart in filter view |
| **Design Principle** | Data labels on bars eliminate the need to read the axis — reduces cognitive load for executives. |
| **Mistake Avoided** | Did NOT use a pie chart for comparative average values. Did NOT omit data labels (which would force axis reading). |

---

## Chart 6 — Discount vs. Profit (Scatter Plot)

| Attribute | Detail |
|---|---|
| **Question Answered** | Is there a relationship between the discount offered and the profit generated? Does discounting hurt profitability? |
| **Why Scatter Plot** | Scatter plots are the canonical tool for visualising correlation between two continuous variables. Each dot = one order, showing the full distribution and outliers. |
| **Fields Used** | X: `discount` (0-35%), Y: `profit` (₹), Color: `category`, Trend Line: linear regression overlay |
| **Design Principle** | Trend line makes the direction of relationship explicit (downward slope = discounting hurts profit). Reference line at Y=0 highlights where orders become unprofitable. |
| **Mistake Avoided** | Did NOT aggregate the data before plotting — aggregation would hide the individual order-level variance and outliers. Did NOT use a line chart for non-sequential data. |

---

## Chart 7 — Return Rate by Category & Region (Grouped Bar)

| Attribute | Detail |
|---|---|
| **Question Answered** | Which category-region combinations have the highest return rates? Where is the return problem concentrated? |
| **Why Grouped Bar** | Two dimensions (category + region) — grouped bars allow both dimensions to be read simultaneously without requiring a mental pivot. |
| **Fields Used** | X: `category`, Groups: `region`, Y: `return_rate` = `return_flag` average (calculated field). Color per region. |
| **Design Principle** | Reference line at overall return rate creates instant benchmark for each bar — above = problem, below = safe. |
| **Mistake Avoided** | Did NOT use a heatmap here — return rates are already percentage values and bars make magnitude comparison easier than colour shading. |

---

## Chart 8 — Shipping Delay Bucket Analysis (Bar + Line Combo)

| Attribute | Detail |
|---|---|
| **Question Answered** | How does delivery speed (bucketed) affect order volume and return rates? Is slower delivery correlated with more returns? |
| **Why Bar + Line Combo** | Bars show volume (count of orders per bucket), while the overlaid line shows the return rate — combining both in one chart reveals a pattern that two separate charts would miss. |
| **Fields Used** | X: `shipping_delay_bucket` (calculated field — categorised from `delivery_days`), Y1 (bar): order count, Y2 (line): return rate |
| **Design Principle** | Dual encoding (bar for count, line for rate) follows the principle of information density — packing two related metrics in one space without confusion. |
| **Mistake Avoided** | Did NOT use two separate charts for this — the relationship between volume and return rate would be harder to spot without them sharing an axis. |

