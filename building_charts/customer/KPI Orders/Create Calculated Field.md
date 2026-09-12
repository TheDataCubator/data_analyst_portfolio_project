# CY Orders

## Purpose
Calculates the total orders for the current year only, filtering out all other years. Used as the numerator/base value in year-over-year comparison calculations and current-year visualizations.

## Formula
```tableau
IF YEAR([Order Date])=[Select Year] THEN [Order ID]
END
```

# PY Orders

## Purpose
Calculates  the total orders for the previous year only, filtering out all other years. Used as the comparison baseline in year-over-year comparison calculations.

## Formula
```tableau
IF YEAR([Order Date])=[Select Year]-1 THEN [Order ID]
END
```

# %Diff Orders

## Purpose
Calculates the year-over-year percentage change in total orders, comparing the current year to the previous year. Used in Total Orders charts to show the order trend directions.

## Formula
```tableau
(COUNTD([CY Orders])-COUNTD([PY  Orders]))/COUNTD([PY  Orders])
```


# Min/Max Orders

## Purpose 
Identifies the highest and lowest total orders within the current year, used to highlight peak and low points in Total Orders charts.


## Formula
```tableau
IF COUNTD([CY Orders])=WINDOW_MAX(COUNTD([CY Orders]))
THEN COUNTD([CY Orders])
ELSEIF COUNTD([CY Orders])=WINDOW_MIN(COUNTD([CY Orders]))
THEN COUNTD([CY Orders])
END
```
