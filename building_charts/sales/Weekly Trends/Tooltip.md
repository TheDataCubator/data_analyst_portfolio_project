# Tooltip

## Purpose
Combines key metrics into a formatted text string for display in chart tooltips, giving viewers additional context when the cursor is pointing at charts.

## Formula
```tableau
No of week: <WEEK(Order Date)>
Sales of <ATTR(Current Year)>: <SUM(CY Sales)>
<AGG(KPI Sales Avg )> the average
Profits of <ATTR(Current Year)>: <SUM(CY Profits)>
<AGG(KPI Profits Avg)> the average
```
