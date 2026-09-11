# KPI Profits Avg

## Purpose 



## Formula
```tableau
IF SUM([Current Year Profits])>WINDOW_AVG(SUM([Current Year Profits]))
THEN 'above'
ELSE 'below'
END
```

# KPI Sales Avg

## Purpose 



## Formula
```tableau
IF SUM([Current Year Sales])>WINDOW_AVG(SUM([Current Year Sales]))
THEN 'above'
ELSE 'below'
END
```
