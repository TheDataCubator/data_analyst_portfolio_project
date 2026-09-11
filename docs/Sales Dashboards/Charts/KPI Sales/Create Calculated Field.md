# Current Year

## Purpose
To create the current year dimension

## Formula
```tableau
[Select Year]
```
After that, change the Current Year to a dimension

# Previous Year

## Purpose
To create the previous year dimension

## Formula
```tableau
[Select Year]-1
```
After that, change Previous Year to a dimension

#CY Sales

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

## Formula
```tableau
(SUM([CY Sales])-SUM([PY Sales]))/SUM([PY Sales])
```

# Min/Max Sales

## Formula
```tableau
(SUM([CY Sales])-SUM([PY Sales]))/SUM([PY Sales])
```
