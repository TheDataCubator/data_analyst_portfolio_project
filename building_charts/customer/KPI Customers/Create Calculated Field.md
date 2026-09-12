# CY Customer

## Purpose
Calculates the total number of unique customers for the current year only, filtering out all other years. Used as the numerator/base value in year-over-year comparison calculations and current-year visualizations.

## Formula
```tableau
IF YEAR([Order Date])=[Select Year] THEN [Customer ID]
END
```

# PY Customer

## Purpose
Calculates  the total number of unique customers for the previous year only, filtering out all other years. Used as the comparison baseline in year-over-year comparison calculations.

## Formula
```tableau
IF YEAR([Order Date])=[Select Year]-1 THEN [Customer ID]
END
```

# %Diff Customer

## Purpose
Calculates the year-over-year percentage change in customers, comparing the current year to the previous year. Used in Total Customers charts to show profit trend directions.

## Formula
```tableau
(COUNTD([CY Customer])-COUNTD([PY Customer]))/COUNTD([PY Customer])
```


# Min/Max Customer

## Purpose 
Identifies the highest and lowest number of customers within the current year, used to highlight peak and low points in Total Customers charts.


## Formula
```tableau
IF COUNTD([CY Customer])=WINDOW_MAX(COUNTD([CY Customer]))
THEN COUNTD([CY Customer])
ELSEIF COUNTD([CY Customer])=WINDOW_MIN(COUNTD([CY Customer]))
THEN COUNTD([CY Customer])
END
```
