# Power BI Data Model

## Version 1
Use one table named `Customer Data`. Each row represents one customer journey/session record.

## Core Fields
Customer ID, customer segment, age group, region, acquisition channel, campaign, visit date, page views, product viewed, add to cart, checkout started, purchase completed, purchase value, session duration, bounce status, feedback score, retention status, funnel stage and conversion status.

## Version 2
A production model can evolve into a star schema with FactCustomerJourney plus DimDate, DimCustomer, DimChannel, DimCampaign, DimRegion and DimProduct.
