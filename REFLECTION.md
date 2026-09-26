# Reflection

GitHub Copilot was useful during the development of the BrewMetrics BI solution because it helped me create and understand DAX measures more quickly. It provided suggestions for Month-over-Month Sales Growth, Running Total Sales, City Sales Rank using RANKX, and Average Sales per Transaction. These suggestions helped me understand how the measures could be implemented in the Power BI data model.

I also learned that Copilot suggestions need to be checked before using them. For the Average Sales per Transaction measure, my initial approach used COUNTROWS to calculate the number of transactions. After checking the data model, I corrected the calculation to use DISTINCTCOUNT with the transaction identifier. This showed me the importance of validating AI-generated suggestions against the actual dataset and model.

Using GitHub and maintaining a full commit history also changed my workflow. Instead of making all changes at once, I could commit the schema, DAX measures, dashboard, and documentation separately. This made the development process easier to track and review. The commit history provides a clear record of how the BI solution developed from the initial data model to the final dashboard and documentation.
