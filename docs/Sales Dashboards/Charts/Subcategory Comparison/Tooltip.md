# Tooltip

## Purpose
Combines key metrics into a formatted text string for display in chart tooltips, giving viewers additional context when the cursor is pointing at charts.

## Formula
```tableau
Sub-Category:	<Sub-Category>
Sales of <ATTR(Current Year)>: <SUM(CY Sales)>
Sales of <ATTR(Previous Year)>: <SUM(PY Sales)>
%Diff Sales: <AGG(%Diff Sales)>
Profits of <ATTR(Current Year)> : <SUM(CY Profits)>
```
