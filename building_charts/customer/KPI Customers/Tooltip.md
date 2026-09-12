# Tooltip

## Purpose
Combines key metrics into a formatted text string for display in chart tooltips, giving viewers additional context when the cursor is pointing at charts.

## Formula
```tableau
No of customers of <MONTH(Order Date)>,<ATTR(Current Year)>: <CNTD(CY Customer)>
No of customers of <MONTH(Order Date)>,<ATTR(Previous Year)>: <CNTD(PY Customer)>
Customer differences: <AGG(%Diff Customer)>
Highest/Lowest customers: <AGG(Min/Max Customer)>
```
