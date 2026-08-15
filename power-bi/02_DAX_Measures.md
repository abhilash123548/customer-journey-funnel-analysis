# Power BI DAX Measures

Assume the imported table is named `Customer Data`.

```DAX
Total Visitors = DISTINCTCOUNT('Customer Data'[Customer ID])

Product Views = CALCULATE(DISTINCTCOUNT('Customer Data'[Customer ID]), 'Customer Data'[Product Viewed] <> BLANK())

Leads Generated = CALCULATE(DISTINCTCOUNT('Customer Data'[Customer ID]), 'Customer Data'[Add to Cart] = 1)

Total Checkouts = CALCULATE(DISTINCTCOUNT('Customer Data'[Customer ID]), 'Customer Data'[Checkout Started] = 1)

Total Purchases = CALCULATE(DISTINCTCOUNT('Customer Data'[Customer ID]), 'Customer Data'[Purchase Completed] = 1)

Total Revenue = SUM('Customer Data'[Purchase Value])

Conversion Rate = DIVIDE([Total Purchases], [Total Visitors], 0)

Add to Cart Rate = DIVIDE([Leads Generated], [Total Visitors], 0)

Checkout Rate = DIVIDE([Total Checkouts], [Leads Generated], 0)

Purchase From Checkout Rate = DIVIDE([Total Purchases], [Total Checkouts], 0)

Average Purchase Value = DIVIDE([Total Revenue], [Total Purchases], 0)

Revenue Per Visitor = DIVIDE([Total Revenue], [Total Visitors], 0)

Retained Customers = CALCULATE(DISTINCTCOUNT('Customer Data'[Customer ID]), 'Customer Data'[Customer Retention Status] = "Retained")

Retention Rate = DIVIDE([Retained Customers], [Total Purchases], 0)

Bounce Rate = DIVIDE(CALCULATE(DISTINCTCOUNT('Customer Data'[Customer ID]), 'Customer Data'[Bounce Status] = "Yes"), [Total Visitors], 0)

Average Session Duration = AVERAGE('Customer Data'[Session Duration])

Average Feedback Score = AVERAGE('Customer Data'[Customer Feedback Score])

Product View Rate = DIVIDE([Product Views], [Total Visitors], 0)

Cart From Product View Rate = DIVIDE([Leads Generated], [Product Views], 0)

Checkout From Cart Rate = DIVIDE([Total Checkouts], [Leads Generated], 0)

Visit To Product View Dropoff = 1 - [Product View Rate]

Product View To Cart Dropoff = 1 - [Cart From Product View Rate]

Cart To Checkout Dropoff = 1 - [Checkout From Cart Rate]

Checkout To Purchase Dropoff = 1 - [Purchase From Checkout Rate]
```

## CAC
CAC cannot be calculated from this dataset because campaign spend is absent. Once spend is added:

```DAX
CAC = DIVIDE([Marketing Spend], [New Customers Acquired], 0)
```
