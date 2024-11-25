---
layout: post
title: World Bank API Poverty Indicators
subtitle: Looking at Specific Countries
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/world_bank.png
share-img: /assets/img/path.jpg
tags: 
author: Sienna Correia
---

![world bank](/assets/img/world_bank.png)

## Selected Countries and Years:
Countries: India, Brazil, US, Germany, Argentina, Colombia, Sweden, Italy, Japan, Mexico
Years: 2020-2022

## Steps:
XX

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
I chose these countries—Argentina, Brazil, Colombia, Germany, India, Italy, Japan, Mexico, Sweden, and the United States—because they represent a diverse mix of developed and developing nations across various continents, offering valuable insights into global poverty trends, income distribution, and economic challenges.

### Results: 
Argentina shows a decrease in the poverty gap from 2020 to 2022 and a similar decrease in the poverty headcount at the national poverty line.
Brazil has an increase in the poverty gap in 2021, but a slight decrease in 2022. The national poverty line data is missing for 2020.
Colombia has data for all years but shows fluctuations in the poverty gap and income share.
Germany, India, Italy, and Japan have incomplete data for 2021 and 2022.
Mexico has some missing data in 2021, but 2022 shows an improvement in the poverty gap and a decrease in the national poverty line.
Sweden has consistent data showing a relatively low poverty gap and income share for the lowest income groups.
United States has a stable poverty gap and a decreasing poverty headcount in 2021, but data is missing for 2022.

## world_bank_poverty_data.csv
> Country,country_iso3,Year,Poverty Gap ($2.15 a day),Income Share (Lowest 10%),Income Share (Lowest 20%),Poverty Headcount ($2.15 a day),Poverty Headcount (National Poverty Lines)
> 
> Argentina,ARG,2020,0.4,1.7,4.7,1.2,42
> Argentina,ARG,2021,0.4,1.8,5,0.9,37.3
> Argentina,ARG,2022,0.2,2,5.4,0.6,39.2
> 
> Brazil,BRA,2020,0.7,1.6,4.5,2,
> Brazil,BRA,2021,2.1,1,3.3,5.8,
> Brazil,BRA,2022,1.2,1.2,3.6,3.5,
> 
> Colombia,COL,2020,4.4,0.9,3.1,9.4,
> Colombia,COL,2021,2.9,1,3.1,7.3,39.7
> Colombia,COL,2022,2.4,1,3.2,6,36.6
> 
> Germany,DEU,2020,0.2,2.9,7.8,0.2,16
> Germany,DEU,2021,,,,,14.8
> Germany,DEU,2022,,,,,
> 
> India,IND,2020,3.4,3.2,7.7,15.5,
> India,IND,2021,2.7,3.3,8,12.9,
> India,IND,2022,,,,,
> 
> Italy,ITA,2020,0.6,2.1,6.3,0.8,20.1
> Italy,ITA,2021,0.6,2.3,6.5,0.8,20.1
> Italy,ITA,2022,,,,,
> 
> Japan,JPN,2020,,,,,
> Japan,JPN,2021,,,,,
> Japan,JPN,2022,,,,,
> 
> Mexico,MEX,2020,0.6,2,5.3,2.1,43.9
> Mexico,MEX,2021,,,,,
> Mexico,MEX,2022,0.3,2.1,5.6,1.2,36.3
> 
> Sweden,SWE,2020,0.3,3,8.2,0.4,15.7
> Sweden,SWE,2021,0.4,2.8,7.8,0.6,16
> Sweden,SWE,2022,,,,,16.1
> 
> United States,USA,2020,0.2,2,5.7,0.2,
> United States,USA,2021,0.2,2.3,6.1,0.2,
> United States,USA,2022,1,1.8,5.2,1.2,

