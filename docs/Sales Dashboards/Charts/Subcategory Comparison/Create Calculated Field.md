# KPI CY Less PY

## Purpose 
Flags subcategories where current year sales are lower than previous year sales, returning an indicator value used to display a small circle marker on the chart — highlighting underperforming subcategories at a glance.


## Formula
```tableau
IF SUM([CY Sales])<SUM([PY Sales]) THEN '⬤' 
ELSE ''
END
```
