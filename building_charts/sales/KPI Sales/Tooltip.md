# Tooltip

## Purpose
Combines key metrics into a formatted text string for display in chart tooltips, giving viewers additional context when the cursor is pointing at charts.

## Formula
```tableau
Sales of <MONTH(Order Date)>,<ATTR(Current Year)>: <SUM(CY Sales)>
Sales of <MONTH(Order Date)>,<ATTR(Previous Year)>: <SUM(PY Sales)>
Sales Differences: <AGG(%Diff Sales)>
Highest/Lowest Sales: <AGG(Min/Max Sales)>
```

