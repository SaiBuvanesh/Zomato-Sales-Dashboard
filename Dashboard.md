# 📈 Dashboard & Analytics

Here’s a breakdown of the dashboard features, the core KPIs we track, and the behind-the-scenes DAX engineering required to bring the data to life. No fluff—just the exact metrics we built.

---

## 🎯 Key Performance Indicators (KPIs)

At the top level, we track the most critical metrics that define business health. These offer an immediate read on performance without getting bogged down in tables.

- **Sales & Orders:** Tracking overall revenue (`Sales`) and total transaction volume (`Order Count`).
- **Customer Acquisition & Retention:** Measuring our true user base through `ActiveUsers` and `UserCount`, while tracking churn and growth via `GainCust` (Gained Customers) and `LostCust` (Lost Customers).
- **Year-over-Year Growth:** Comparing current performance against historical data (`CurrYearSale` vs `PrevYearSale`) to understand long-term trends and momentum.
- **Top Performers:** Isolating the best-selling items, top cuisines, or top restaurants utilizing the `TOPN Sale` metric.
- **Customer Satisfaction:** Capturing the volume of feedback via `Rating Count`.

---

## 🎛️ Slicers & Interactivity

We built the dashboard to be highly interactive so anyone can slice and dice the data dynamically on the fly:

- **Time/Date Slicers:** Filter by specific years or quarters to spot seasonal trends (`CurrYr`, `PrevYr`).
- **City / Region:** Drill down into specific geographic performance.
- **Cuisine / Food Category:** View how Veg vs. Non-Veg orders stack up, or filter by specific cuisine types.

---

## 🧮 Core DAX Measures (The Engine)

We wrote a comprehensive suite of DAX (Data Analysis Expressions) formulas to calculate dynamic, contextual values. Based on the data model, here are the precise measures driving the visual architecture:

### 💰 Core Sales & Volume
- `Sales`: Total revenue generated across all selected criteria.
- `Order Count`: The total volume of orders placed.
- `Rating Count`: The volume of ratings submitted.

### 👥 Customer Insights (Retention Engine)
Our true analytical power comes from tracking user behavior across timeframes.
- `ActiveUsers` / `UserCount`: Distinct counts of users engaging with the platform.
- `GainCust`: Calculates the number of newly acquired or returning customers within a specific period.
- `LostCust`: Identifies churned users who haven't ordered within the specified timeframe.

### ⏱️ Time Intelligence
- `CurrYearSale`: Dynamically calculates sales for the currently filtered year.
- `PrevYearSale`: Returns the sales corresponding to the prior year.
- `CurrYr` & `PrevYr`: Year identifiers dynamically updating our charts and visual labels.

### 📊 Dynamic Visuals & Advanced Filtering
- `BarChartVisual` & `LineChartVisual`: Dedicated measures designed to dynamically feed interactive slices of data directly into our charting tools.
- `TOPN Sale`: Re-calculates and restricts visibility exclusively to the top performers evaluated by Sales.

---

## 🎨 Design & UI

To make it look premium and easy to consume:
- **Clean Palette:** We used a modern, high-contrast color palette to emphasize the data.
- **Custom Icons:** Visual cues from the `Images/` folder were integrated for KPIs and navigation elements.
- **Smart Tooltips:** Implemented rich tooltips so hovering over charts provides deeper context without cluttering the screen real estate.
