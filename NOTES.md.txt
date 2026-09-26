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

## Measure 2 – Running Total Sales

Copilot suggested a DAX measure to calculate the running total of sales over time.

The suggested formula was reviewed and used after checking it with the Dim_Date table and Total Sales measure.

The measure was tested in Power BI using a date-based visual, and the running total increased cumulatively over time.

## Measure 3 – City Sales Rank

Copilot suggested a RANKX measure to rank cities based on Total Sales.

The suggested measure uses ALL(Dim_City[city]) to compare all cities, DESC to rank the highest sales as rank 1, and DENSE for consecutive ranking when there are ties.

I checked the measure against the city field and Total Sales measure and used the generated formula in the Power BI model.

## Measure 4 – Average Sales per Transaction

### Copilot Suggestion

My initial approach used COUNTROWS to calculate the average sales per transaction:

```DAX
Average Transaction Value =
DIVIDE(
    [Total Sales],
    COUNTROWS(Fact_Sales)
)

## Correction

After checking the data model, Copilot identified Fact_Sales[sale_id] as the transaction identifier. Therefore, the COUNTROWS approach was changed to DISTINCTCOUNT so that unique transactions are counted.

The corrected measure is:

Average Sales per Transaction =
DIVIDE(
    [Total Sales],
    DISTINCTCOUNT(Fact_Sales[sale_id])
)

The corrected measure was entered in Power BI and tested successfully using a Card visual.

This corrected measure was used as the final Measure 4 in the Power BI report