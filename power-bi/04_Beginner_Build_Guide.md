# Beginner Power BI Build Guide

1. Open Power BI Desktop.
2. Home → Get Data → Text/CSV.
3. Import `customer_journey_funnel_dataset_150_rows.csv`.
4. Rename the table to `Customer Data`.
5. Set Website Visit Date to Date; Page Views, Add to Cart, Checkout Started and Purchase Completed to Whole Number; Purchase Value and Feedback Score to Decimal.
6. Create the measures in `02_DAX_Measures.md` using Modeling → New measure.
7. Create five KPI Cards.
8. Add a Funnel visual using Funnel Stage and a distinct customer count.
9. Add channel conversion bar chart.
10. Add segment/region performance charts.
11. Add retention stacked column chart.
12. Add drop-off measures as a bar chart.
13. Add slicers for date, channel, segment, region, campaign and age group.
14. Apply consistent typography, spacing, titles and alignment.
15. Validate all slicers and measures.
16. Save as `Customer_Journey_Funnel_Dashboard.pbix`.
17. Export screenshots to `dashboard/screenshots/`.
