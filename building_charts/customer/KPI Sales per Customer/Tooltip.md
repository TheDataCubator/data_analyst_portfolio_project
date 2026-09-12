# Tooltip

## Purpose
Combines key metrics into a formatted text string for display in chart tooltips, giving viewers additional context when the cursor is pointing at charts.

## Formula
```tableau
Sales per Customer of <MONTH(Order Date)>,<ATTR(Current Year)>: <AGG(CY Sales per Customer)>
Sales per Customer of <MONTH(Order Date)>,<ATTR(Previous Year)>: <AGG(PY Sales per Customer)>
Sales Per Customer differences:	<AGG(%Diff Sales Per Customer)>
Highest/Lowest sales per customer:	<AGG(Min/Max Sales per Customer)>
```
