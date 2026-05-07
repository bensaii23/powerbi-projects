# European Inflation Monitor — Power BI Dashboard

## Overview

This project is an interactive Power BI dashboard that analyzes annual inflation trends across selected countries using World Bank data.
The objective is to explore how inflation evolved over time, compare inflation levels between countries, and identify periods of high inflation. 
The dashboard was created as a first Power BI project to practice data cleaning, transformation, visualization, and dashboard design using real-world economic data.

## Project Objectives

The main objectives of this project are to:

- Analyze annual consumer price inflation across selected countries
- Compare inflation trends over time
- Identify countries with the highest and lowest inflation levels
- Build an interactive dashboard using Power BI
- Practice data cleaning and transformation using Power Query
- Present economic data in a clear and accessible way

## Dataset

The dataset comes from the World Bank Open Data platform.
**Indicator used:** Inflation, consumer prices (annual %)  
**Indicator code:** `FP.CPI.TOTL.ZG`  
**Source:** World Bank World Development Indicators

The data contains annual inflation rates by country, with years originally stored as separate columns. The dataset was reshaped in Power Query to make it suitable for visualization in Power BI.

## Tools Used

- Power BI Desktop
- Power Query
- World Bank Open Data

## Data Preparation

The original dataset was provided in a wide format, where each year appeared as a separate column.

Example of original structure:

| Country Name | Country Code | 2019 | 2020 | 2021 | 2022 |
|---|---|---:|---:|---:|---:|
| France | FRA | 1.1 | 0.5 | 2.1 | 5.2 |
| Germany | DEU | 1.4 | 0.5 | 3.1 | 6.9 |

This structure was transformed into a long format using Power Query.

Example of cleaned structure:

| Country | Country Code | Year | Inflation |
|---|---|---:|---:|
| France | FRA | 2019 | 1.1 |
| France | FRA | 2020 | 0.5 |
| France | FRA | 2021 | 2.1 |
| France | FRA | 2022 | 5.2 |
| Germany | DEU | 2019 | 1.4 |
| Germany | DEU | 2020 | 0.5 |

Main cleaning steps:

- Imported the World Bank CSV file into Power BI
- Removed unnecessary columns
- Unpivoted year columns into a single `Year` column
- Renamed columns for readability
- Converted data types:
  - `Year` as whole number
  - `Inflation` as decimal number
- Removed null inflation values
- Filtered the dataset to selected countries and years

## Dashboard Features

The Power BI dashboard includes:

- Interactive country filter
- Interactive year filter
- Line chart showing inflation trends over time
- Bar chart comparing average inflation by country
- KPI cards showing:
  - Average inflation
  - Maximum inflation
  - Minimum inflation

## Key Insights

Some insights that can be observed from the dashboard:

1. Inflation increased significantly in many countries after 2020.
2. Inflation levels vary strongly between countries.
3. Some countries show more stable inflation trends, while others experience higher volatility.
4. The year filter allows users to focus on specific periods, such as the post-2020 inflation increase.
5. The country filter makes it easier to compare selected countries directly.
