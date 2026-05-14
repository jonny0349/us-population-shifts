# The Changing Face of America
### Exploratory Analysis of County-Level Demographic Shifts (2019-2024)

## Overview

This project is an exploratory data analysis of county-level demographic change across the United States between 2019 and 2024. Using the U.S. Census Bureau's American Community Survey
(ACS) 1-Year Demographic Profile table DP05, we examine how American counties are shifting in population shize, age structure, racial composition, sex ratio, and housing availability over
a five-year window that spans the COVID-19 pandemic and its aftermath. 

The analysis was originally developed as a capstone project for INSS615: Data Wrangling for Visualization at Morgan State University and has since been refactored into a portfolio-quality
exploratory analysis with a clear pipeline, expanded EDA, and ning ggplot2 visualizations.

## Data Source

**U.S. Census Bureau - American Community Survey 1-Year Estimates, Table DP05**
- Survey years: 2019, 2021, 2022, 2023, 2024 (2020 was not released due to COVID-19 pandemic disruptions)
- Geography: All U.S. counties and county-equivalents with populations of 65,000 or more
- Download: [data.census.gov](https://data.census.gov/table/ACSDP1Y2024.DP05)

Five separate CSV files must be downloaded, one per survey year, filtered to all U.S. counties.

## Tools

- **R** and **R Markdown**
- **Tidyverse** - data wrangling and visualization (dplyr, tidyr, stringr, ggplot2)
- **here** - reproducible file paths
- **scales** - axis formatting in ggplot2

## Project Structure

```
us-population-shifts/
├── README.md
├── .gitignore
├── us-population-shifts.Rproj
├── us-population-shifts.Rmd
├── data/
│   └── raw/
│       ├── 2019/
│       ├── 2021/
│       ├── 2022/
│       ├── 2023/
│       └── 2024/
└── output/
```

## How to Reproduce 

1. Clone this repository
2. Download the ACS DP05 1-Year Estimates CSV files for 2019, 2021, 2022, 2023, and 2024, from [data.census.gov](https://data.census.gov/table/ACSDP1Y2024.DP05)
3. Place each year's files in the corresponding folder under `data/raw/`
4. Open `us-population-shifts.Rproj` in Rstudio or Positron.
5. Open `us-population-shifts.Rmd` and knit to HMTL

## Analysis Structure

- **Data Acquisition** - loading five raw ACS CSV files with controlled column types
- **Initial Exploration** - dimensions, structure, and raw data inspection before any transformation
- **Cleaning & Transformation** - special value replacement, type conversion, geographic parsing, and regional classification using U.S. Census Bureau region and division definitions
- **Exploratory Data Analysis** - distributions of population, median age, sex ratio, missing data patterns, and county coverage across years and regions
- **Derived Variables** - six engineered variables included senior population share, working age share, youth share, population change tier, racial diversity index, and housing to population ratio
- **Visualizations** - nine ggplot2 charts covering age structure trends, population growth patterns, racial diversity, housing supply, and the intersections between these dimensions

## Authos
Jonatan Tobón González
Morgan State University - Department of Information Science & Systems