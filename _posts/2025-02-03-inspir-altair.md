---
layout: post
title: Inspir Altair Cool Visualizations!
subtitle: Women in Songwriting & Ivy League Women's Soccer Standings
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/world_bank.png
share-img: /assets/img/path.jpg
tags: 
author: Sienna Correia
---

![world bank](/assets/img/world_bank.png)

## Selected Countries and Years:

## Steps:
Identifying My Indicator Codes:
I clicked on different indicators to reveal their unique codes (ex. SI.POV.DDAY for Poverty headcount ratio at $2.15 a day), which I reused directly in my Python code for constructing the API endpoint.
   
https://api.worldbank.org/v2/country?format=json&per_page=300

To fetch a complete list of all countries, including their ISO3 codes and names, as a starting point for selecting relevant countries.

https://api.worldbank.org/v2/country/{country_iso3}?format=json

To retrieve detailed data (ex. country name) for a specific country using its ISO3 code during runtime.

https://api.worldbank.org/v2/country/{country_iso3}/indicator/{indicator}

To fetch poverty-related indicator data for a specific country and year, based on its ISO3 code and the chosen indicator. Applied this to each country and year of choice. For example, produced data on India’s poverty gap in 2020.

## CSV Data Attributes
Country: The name of the country.

country_iso3: The ISO-3 country code (e.g., ARG for Argentina).

Year: The year of the data.

Poverty Gap ($2.15 a day): The average shortfall of income of the population living below $2.15 a day.

Income Share (Lowest 10%): The share of income held by the lowest 10% of the population.

Income Share (Lowest 20%): The share of income held by the lowest 20% of the population.

Poverty Headcount ($2.15 a day): The percentage of the population living below $2.15 a day.

Poverty Headcount (National Poverty Lines): The percentage of the population living below the national poverty line.

## Selection and Results
### Selection: 
I chose these countries—Argentina, Brazil, Colombia, Germany, India, Italy, Japan, Mexico, Sweden, and the United States—because they represent a diverse mix of developed and developing nations across various continents, offering valuable insights into global poverty trends, income distribution, and economic challenges. I chose a 10 year range from 2012 to 2022, allowing for a considerate number of years to better understand trends.  

### Results: 
#### Countries with Decreasing Poverty Over the Decade
   
Argentina: A steady decline in the poverty gap from 0.3 in 2012 to 0.2 in 2022. The national poverty headcount also dropped significantly, from highs of 42.0% in 2020 to 39.2% in 2022.

India: Marked reductions in poverty indicators, with the headcount at $2.15/day decreasing from 18.8% in 2015 to 12.9% in 2021. Although 2022 data is missing, the overall trend suggests consistent improvement.

Mexico: A slight decline in the poverty gap, from 1.2 in 2012 to 0.3 in 2022, alongside a reduction in the national poverty headcount, which fell to 36.3% by 2022.


#### Countries with Stable Low Poverty
   
Germany: Consistently low poverty gap (0–0.2) and poverty headcount at $2.15/day (~0%), with a stable national poverty headcount around 16%.

Sweden: Maintains a low poverty gap (0.1–0.6) and stable income share for the lowest groups. The national poverty headcount remains near 16% throughout the decade, reflecting strong economic equality.


#### Countries with Fluctuating Trends
   
Brazil: Shows variations in the poverty gap, peaking at 2.1 in 2021 before improving to 1.2 in 2022. However, the poverty headcount at $2.15/day fluctuates without a clear long-term trend. National poverty line data is notably missing for some key years (2020).

Colombia: Experiences a spike in the poverty gap in 2020 (4.4) during global economic challenges but shows improvement by 2022 (2.4). The national poverty headcount decreases from 39.7% in 2021 to 36.6% in 2022, indicating recovery.


#### Countries with Incomplete or Inconsistent Data
   
Italy: Relatively stable indicators through 2019, but data for 2021 and 2022 is missing. The national poverty headcount fluctuated slightly, ranging around 19–20% until 2020.

Japan: Sparse data across the decade, especially for 2021 and 2022. Earlier years suggest very low poverty levels.

United States: The poverty gap remained stable (~0.8–1.0) with a slight decrease in the poverty headcount in 2021, but missing data for 2022 limits recent analysis.


## P-Value Analysis
I chose to look at 3 different relationships: a highly significant p-value, significant p-value, and not significant p-value

### Highly Significant: 

#### (Independent) Poverty Gap ($2.15 a day) vs. (Dependent) Poverty Headcount ($2.15 a day)
#### p-value = 0.0, slope = 3.7888

The p-value of 0.0 indicates an extremely strong statistical relationship between the poverty gap and the poverty headcount at $2.15 a day. As the gap widens, it shows that not only are more people below the line but that they are further from escaping it, naturally correlating with a higher poverty headcount. A positive slope of 3.7888 suggests that as the poverty gap increases, the proportion of people living below the $2.15 threshold rises substantially.

### Significant:

#### (Independent) Poverty Gap ($2.15 a day) vs. (Dependent) Income Share (Lowest 10%)
#### p-value = 0.0239, slope = -0.1948

The p-value of 0.0239 indicates a statistically significant relationship. A negative slope of -0.1948 suggests ain inverse relationship that as the poverty gap widens, the share of income held by the lowest 10% decreases.

### Not Significant:

#### (Independent) Income Share (Lowest 20%) vs. (Dependent) Poverty Headcount ($2.15 a day)
#### p-value = 0.6824, slope = -0.1021

The p-value of 0.6824 suggests no statistically significant relationship between the two variables. The slope of -0.1021 implies a weak negative trend, but it is not reliable enough to draw conclusions. While income share and poverty headcount may seem linked, the lack of significance indicates that variations in the income share of the lowest 20% do not consistently correlate with changes in the poverty headcount at $2.15 a day.



