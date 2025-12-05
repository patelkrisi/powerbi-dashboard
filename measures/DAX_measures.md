# DAX Measures

This file contains the key DAX measures used in the Power BI dashboard.

## Revenue
``Revenue = SUM(Sales[Revenue])``

## Total Quantity
``Total Quantity = SUM(Sales[Quantity])``

## Profit
``Profit = SUM(Sales[Profit])``

## Profit Margin %
``Profit Margin % = DIVIDE([Profit], [Revenue], 0)``

## YoY Growth (Example)
``YoY Growth = 
VAR CurrentYear = [Revenue]
VAR PriorYear = CALCULATE([Revenue], DATEADD('Date'[Date], -1, YEAR))
RETURN DIVIDE(CurrentYear - PriorYear, PriorYear)
