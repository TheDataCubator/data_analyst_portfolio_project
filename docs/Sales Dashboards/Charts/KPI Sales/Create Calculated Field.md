# Current Year

## Purpose
To create the current year dimension

## Formula
```tableau
[Select Year]
```
After that, change Current Year to a dimension

# Previous Year

## Purpose
To create the previous year dimension

## Formula
```tableau
[Select Year]-1
```
After that, change Previous Year to a dimension

# CY Sales

## Formula
```tableau
IF YEAR([Order Date])=[Select Year] THEN [Sales]
END
```

# PY Sales

## Formula
```tableau
IF YEAR([Order Date])=[Select Year]-1 THEN [Sales]
END
```

# %Diff Sales

## Purpose
Calculates the year-over-year percentage change in sales, comparing the current year to the previous year. Used in Total Sales charts to show sales trend direction.

## Formula
```tableau
(SUM([CY Sales])-SUM([PY Sales]))/SUM([PY Sales])
```


# Min/Max Sales

## Purpose 
Identifies the highest and lowest sales values within the current year, used to highlight peak and low points in [Total Sales charts].


## Formula
```tableau
IF SUM([CY Sales])=WINDOW_MAX(SUM([CY Sales]))
THEN SUM([CY Sales])
ELSEIF SUM([CY Sales])=WINDOW_MIN(SUM([CY Sales]))
THEN SUM([CY Sales])
END
```
