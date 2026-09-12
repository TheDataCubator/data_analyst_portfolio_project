# Tooltip

## Purpose
Combines key metrics into a formatted text string for display in chart tooltips, giving viewers additional context when the cursor is pointing at charts.

## Formula
```tableau
Total orders of <MONTH(Order Date)>,<ATTR(Current Year)>: <CNTD(CY Orders)>	
Total orders of <MONTH(Order Date)>,<ATTR(Previous Year)>: <CNTD(PY  Orders)>
Total order diferences: <AGG(%Diff Order)>
Highest/Lowest Orders: <AGG(Min/Max Orders)>
```
