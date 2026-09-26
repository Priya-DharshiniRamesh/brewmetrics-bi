# DAX Development Notes
# Copilot Notes

## Measure 1: Month-over-Month Sales Growth

### Copilot Suggestion

GitHub Copilot checked the existing `Fact_Sales.tmdl` file and identified a month-over-month sales growth measure:

```DAX
MoM Sales Growth % =
VAR PreviousMonthSales =
    CALCULATE(
        [Total Sales],
        PREVIOUSMONTH('Dim_Date'[date])
    )
RETURN
    DIVIDE([Total Sales] - PreviousMonthSales, PreviousMonthSales)