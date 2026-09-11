# Current Year

## Purpose
Determines the most recent year present in the Order Date field, typically based on the maximum year in the dataset, or a selected year if a parameter is used. Used as a reference point to filter or compare other calculated fields.

## Formula
```tableau
[Select Year]
```
After that, change Current Year to a dimension

# Previous Year

## Purpose
Determines the year immediately preceding the current year (Current Year − 1). Used as a reference point for year-over-year comparisons.

## Formula
```tableau
[Select Year]-1
```
After that, change Previous Year to a dimension

# CY Sales

## Purpose
Calculates total sales for the current year only, filtering out all other years. Used as the numerator/base value in year-over-year comparison calculations and current-year visualizations.

## Formula
```tableau
IF YEAR([Order Date])=[Select Year] THEN [Sales]
END
```

# PY Sales

## Purpose
Calculates total sales for the previous year only, filtering out all other years. Used as the comparison baseline in year-over-year comparison calculations.

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
Identifies the highest and lowest sales values within the current year, used to highlight peak and low points in Total Sales charts.


## Formula
```tableau
IF SUM([CY Sales])=WINDOW_MAX(SUM([CY Sales]))
THEN SUM([CY Sales])
ELSEIF SUM([CY Sales])=WINDOW_MIN(SUM([CY Sales]))
THEN SUM([CY Sales])
END
```
