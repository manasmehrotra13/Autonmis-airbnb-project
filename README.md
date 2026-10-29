# Airbnb Market Intelligence: Prices in European Cities

Case study from my data analyst internship at **Autonmis** (early 2025). The data is the public Kaggle dataset "Airbnb Prices in European Cities".

## The data
20 tables (10 European cities, weekdays and weekends), about 52,000 listings: price, room type, guest capacity, distance from the city centre, cleanliness and guest satisfaction scores.

## What I did
- Loaded the 20 tables into PostgreSQL and combined them into one view with `UNION ALL`.
- Wrote 13+ SQL queries:
  - KPIs: revenue, average price per night, revenue per guest, satisfaction
  - city rankings with `DENSE_RANK()`
  - price bands by distance from the centre with `CASE`
  - weekday vs weekend comparisons
  - each city's share of the total with `SUM() OVER()`
  - a simple regression in SQL (`REGR_SLOPE` / `REGR_INTERCEPT`) to estimate how much weekend prices rise in each city
- Built a dashboard on the Autonmis platform and wrote up the case study.

## Tools
PostgreSQL (Neon), SQL (window functions, CTEs, regression functions), the Autonmis platform.

## Files
- `Airbnb Prices in European Cities.zip`: the dataset
- `Autonmis Airbnb.pdf`: the case study write-up
- `Airbnb dashboard.pdf`: the dashboard
- two images
