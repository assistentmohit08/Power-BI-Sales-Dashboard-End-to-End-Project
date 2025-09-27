# Power BI Superstore Sales Dashboard

An interactive **Power BI dashboard** built using the Superstore dataset.  
This project demonstrates **data cleaning, DAX calculations, and a 15-day sales forecast** to analyze business performance across categories, regions, and time.

---

## 📊 Dashboard Overview

![Dashboard Overview](images/dashboard_overview.png)

The dashboard provides a **comprehensive view of sales performance**, including:  
- Sales and profit by region, category, and sub-category  
- Sales by segment and payment mode  
- Regional performance on a map  
- Year-over-Year (YoY) sales and profit trends  
- KPIs with total sales and top contributors  

---

## 🔮 15-Day Sales Forecast

![Forecast View](images/forecast_view.png)

The dashboard includes a **15-day sales forecast** using Power BI's built-in forecasting tool.

- **Methodology:**  
  - Applied forecast on daily sales line chart using the Analytics Pane.  
  - Forecast length: **15 days ahead**.  
  - Confidence interval shown as shaded area for expected fluctuation.  

- **Observations:**  
  - Forecast projects sales around **3K units** in the upcoming 15 days.  
  - Seasonal fluctuations are captured with confidence bounds.  

- **Business Impact:**  
  - Helps predict demand and align inventory.  
  - Useful for marketing and supply chain planning.  

---

## 🧮 DAX Calculations

Key DAX measures created for insights:

```DAX
-- Total Sales
Total Sales = SUM(Superstore[Sales])

-- Year-over-Year Sales
YoY Sales = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))

-- Profit Percentage
Profit % = DIVIDE(SUM(Superstore[Profit]), SUM(Superstore[Sales]))
