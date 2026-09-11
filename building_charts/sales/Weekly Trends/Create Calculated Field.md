# KPI Profits Avg

## Purpose 
Determines the average value within the Weekly Trends chart, then classifies each point as above or below that average. This classification is used to assign distinct colors to the above-average and below-average areas of the Weekly Trends chart.


## Formula
```tableau
IF SUM([Current Year Profits])>WINDOW_AVG(SUM([Current Year Profits]))
THEN 'above'
ELSE 'below'
END
```

# KPI Sales Avg

## Formula
```tableau
IF SUM([Current Year Sales])>WINDOW_AVG(SUM([Current Year Sales]))
THEN 'above'
ELSE 'below'
END
```
