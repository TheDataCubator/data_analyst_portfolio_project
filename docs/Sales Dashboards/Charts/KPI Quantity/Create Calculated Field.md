# CY Quantity

## Purpose
Calculates total quantities for the current year only, filtering out all other years. Used as the numerator/base value in year-over-year comparison calculations and current-year visualizations.

## Formula
```tableau
IF YEAR([Order Date])=[Select Year] THEN [Quantity]
END
```

# PY Quantity

## Purpose
Calculates total quantities for the previous year only, filtering out all other years. Used as the comparison baseline in year-over-year comparison calculations.

## Formula
```tableau
IF YEAR([Order Date])=[Select Year]-1 THEN [Quantity]
END
```

# %Diff Quantity

## Purpose
Calculates the year-over-year percentage change in quantities, comparing the current year to the previous year. Used in Total Quantity charts to show quantity trend directions.

## Formula
```tableau
(SUM([CY Quantity])-SUM([PY Quantity]))/SUM([PY Quantity])
```


# Min/Max Quantity

## Purpose 
Identifies the highest and lowest quantity values within the current year, used to highlight peak and low points in Total Quantity charts.


## Formula
```tableau
IF SUM([CY Quantity])=WINDOW_MAX(SUM([CY Quantity]))
THEN SUM([CY Quantity])
ELSEIF SUM([CY Quantity])=WINDOW_MIN(SUM([CY Quantity]))
THEN SUM([CY Quantity])
END
```
