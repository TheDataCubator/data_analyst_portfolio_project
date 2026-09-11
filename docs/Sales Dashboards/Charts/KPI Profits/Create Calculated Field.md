# CY Profits

## Purpose
Calculates total profits for the current year only, filtering out all other years. Used as the numerator/base value in year-over-year comparison calculations and current-year visualizations.

## Formula
```tableau
IF YEAR([Order Date])=[Select Year] THEN [Profit]
END
```

# PY Profits

## Purpose
Calculates total profits for the previous year only, filtering out all other years. Used as the comparison baseline in year-over-year comparison calculations.

## Formula
```tableau
IF YEAR([Order Date])=[Select Year]-1 THEN [Profit]
END
```

# %Diff Profits

## Purpose
Calculates the year-over-year percentage change in profits, comparing the current year to the previous year. Used in Total Profits charts to show profit trend directions.

## Formula
```tableau
(SUM([CY Profits])-SUM([PY Profits]))/SUM([PY Profits])
```


# Min/Max Profits

## Purpose 
Identifies the highest and lowest profit values within the current year, used to highlight peak and low points in Total Profits charts.


## Formula
```tableau
IF SUM([CY Profits])=WINDOW_MAX(SUM([CY Profits]))
THEN SUM([CY Profits])
ELSEIF SUM([CY Profits])=WINDOW_MIN(SUM([CY Profits]))
THEN SUM([CY Profits])
END
```
