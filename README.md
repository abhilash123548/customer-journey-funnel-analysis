# Customer Journey & Funnel Analysis Dashboard

## Objective
Analyze customer behavior from website visit through purchase and retention, identify funnel bottlenecks, compare acquisition performance, and produce actionable recommendations.

## Business Problem
Marketing and product teams need a single view of where customers drop out, which channels and campaigns convert, which segments generate value, and where retention can improve.

## Dataset Description
Synthetic 150-row customer journey dataset containing acquisition, behavior, funnel, revenue, feedback, and retention fields.

## Funnel Framework
Visit → Product View → Add to Cart → Checkout → Purchase → Retention

## Analysis Performed
- Funnel conversion and drop-off analysis
- Channel and campaign performance
- Customer segmentation
- Regional conversion analysis
- Retention analysis
- Feedback/customer-experience review
- Opportunity identification and recommendations

## Dashboard Features
Recommended final tool: Power BI.
- KPI cards
- Funnel visualization
- Customer journey flow
- Channel performance
- Segment and region analysis
- Retention analysis
- Drop-off analysis
- Interactive slicers

## Power BI Implementation
See [`power-bi/`](power-bi/) for the data model, DAX measures, dashboard specification, and beginner build guide.

## Key Insight Framework
Use the dashboard to identify the largest funnel loss, strongest channels, highest-value segments, weakest campaigns, regional differences, and retention gaps.

## Recommendations
Prioritize the highest funnel bottleneck, scale efficient acquisition sources, optimize low-converting campaigns, improve onboarding/re-engagement, and use feedback to target experience improvements.

## CAC Note
CAC cannot be calculated from the requested dataset because marketing spend is not included. Add a Campaign Spend field before reporting CAC.

## Conclusion
The project demonstrates how a Business Analyst converts customer journey data into management-ready insights and actions.
