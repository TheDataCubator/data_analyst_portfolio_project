# Tooltip

## Purpose
Combines key metrics into a formatted text string for display in chart tooltips, giving viewers additional context when the cursor is pointing at charts.

## Formula
```tableau
Profits of <MONTH(Order Date)>,<ATTR(Current Year)>: <SUM(CY Quantity)>
Profits of <MONTH(Order Date)>,<ATTR(Previous Year)>: <SUM(PY Quantity)>
Profits Differences: <AGG(%Diff Quantity)>
Highest/Lowest Profits: <AGG(Min/Max Quantity)>
```
