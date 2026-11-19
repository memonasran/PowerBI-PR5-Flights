# Power BI PR5 — Flight Delay and Cancellation Dashboard

## Project Overview
This project builds an interactive 5-page dashboard in Power BI using the
Flight Delay and Cancellation Dataset (2019-2023) from Kaggle.

## Dataset
-**Name:** Flight Delay and Cancellation Dataset (2019-2023)
-**Author:** Patrick Zelazko
-**Kaggle URL:** https://www.kaggle.com/datasets/patrickzel/flight-delay-and-cancellation-dataset-2019-2023
-**File:** flights_sample_3m.csv (3,000,000 rows)

## Measures (6)
| Measure | Formula | Business Use |
| :--- | :--- | :--- |
| Total_Flights | COUNTROWS(FlightData) | Baseline KPI |
| Total_Cancelled | CALCULATE(COUNTROWS, CANCELLED=1) | Cancellation count |
| Cancellation_Rate% | DIVIDE(Total_Cancelled, Total_Flights) | % cancelled |
| Avg_Dep_Delay | AVERAGEX(FILTER(non-cancelled), DEP_DELAY) | Avg departure delay |
| Avg_Arr_Delay | AVERAGEX(FILTER(non-cancelled), ARR_DELAY) | Avg arrival delay |
| On_Time_Rate% | DIVIDE(on-time, operated) | % on-time |

## Calculated Column
-Delay_Category: SWITCH(TRUE(), ...) – classifies flights into Cancelled, Diverted, Major Delay, Minor Delay, On Time.

## Report Pages
1.Overview
2.Airline Performance
3.Route & Airport Map
4.Drill-Through Detail
5.Trends & Forecast

## Features
-Drill-through to airline detail
-Custom navigation bar
-Slicer panel with bookmarks
-Fields parameter to switch metrics
-Custom tooltip page
-Mobile layout
-Numeric range parameter

## Tools Used
-Power BI Desktop
-Power Query
-DAX

## Screenshots
(Add screenshots of all 5 pages, mobile layout, and model view)

## Video Link
(Add your video link here)
