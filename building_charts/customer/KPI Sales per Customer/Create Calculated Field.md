# CY Sales per Customer

## Purpose
Calculates the total sales per customer for the current year only, filtering out all other years. Used as the numerator/base value in year-over-year comparison calculations and current-year visualizations.

## Formula
```tableau
SUM([CY Sales])/COUNTD([CY Customer])
```

# PY Sales per Customer

## Purpose
Calculates the total sales per customer for the previous year only, filtering out all other years. Used as the comparison baseline in year-over-year comparison calculations.

## Formula
```tableau
SUM([PY Sales])/COUNTD([PY Customer])
```

# %Diff Sales per Customer

## Purpose
Calculates the year-over-year percentage change in total sales per customer, comparing the current year to the previous year. Used in Total Sales per Customer charts to show the total sales per customer trend directions.

## Formula
```tableau
([CY Sales per Customer]-[PY Sales per Customer])/[PY Sales per Customer]
```


# Min/Max Sales per Customer

## Purpose 
Identifies the highest and lowest number of total sales per customer within the current year, used to highlight peak and low points in Total Sales per Customer charts.


## Formula
```tableau
IF ([CY Sales per Customer])=WINDOW_MAX(([CY Sales per Customer]))
THEN ([CY Sales per Customer])
ELSEIF ([CY Sales per Customer])=WINDOW_MIN(([CY Sales per Customer]))
THEN ([CY Sales per Customer])
END
```
