---
layout: post
title: Final Art of Data Project
subtitle: The Barriers to Mobility for Black Americans (Incarceration and Economic Disparities) 
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/jail_image.jpg
share-img: /assets/img/path.jpg
tags: 
author: Sienna Correia
---

# Introduction:
  For my final project, I decided to investigate the barriers to upward mobility for Black Americans, with a particular focus on incarceration and related economic disparities in education, employment, and income, I was inspired by my legal history research paper on the 1960s War on Poverty and its unintended role in fueling incarceration. That research led me to wonder: How have these long-tern systems continued to shape opportunities for the next generation? 
  To ground this inquiry in data, I explored multiple sources and learned how to visualize patterns across gender, race, and income level. My goal was to uncover how mobility outcomes differ for Black and White children, especially those from low-income families. This led me to my hypothesis!

Hypothesis: Black American children face greater barriers to both economic and educational mobility than their White peers, even when starting at similar parental income levels. These barriers—measured by differences in incarceration risk, college completion rates, employment at age 30, and relative wage rank—persist across the income distribution and are especially pronounced at lower and middle percentiles. 

# Data:

#### 1. Incarceration Over Time
Initially, I explored incarceration counts by race from 1978 to 2011 using data from the Inter-university Consortium for Political and Social Research (ICPSR), part of the University of Michigan. However, I realized raw numbers were misleading due to differences in population sizes between racial groups. I then calculated percent of each racial group incarcerated, using population data from USAFacts, which aggregates government sources. 

### Incarceration Counts Over Time by Race (1978–2011) 
![Incarceration Counts Over Time by Race (1978–2011) Visualization](/assets/img/Incarceration Counts Over Time by Race (1978–2011).png)

### Percent of Racial Group Incarcerated (1978 vs 2011)
<head>
  <!-- Import Vega & Vega-Lite (does not have to be from CDN) -->
  <script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
  <!-- Import vega-embed -->
  <script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>
</head>

<div id="vis"></div>
<script type="text/javascript">
  var spec = "https://raw.githubusercontent.com/siennacorreia/siennacorreia.github.io/refs/heads/master/assets/Percent of Racial Group Incarcerated (1978 vs 2011).json";
  vegaEmbed('#vis', spec).then(function(result) {
    // Access the Vega view instance (https://vega.github.io/vega/docs/api/view/) as result.view
  }).catch(console.error);
</script>

#### 2. Poverty Rates By Race
To further explore economic disparity, I compared the recent poverty rates for Black and White Americans. Though the timeline (2022-2023) differs from earlier data, the persistent racial wealth gap is clear. This data came from the United States Census Bureau, which conducts the nation’s largest population survey.

### Poverty Rate Over Time by Race (Black vs. White) (2022-2023)
![Poverty Rate Over Time by Race (Black vs. White) (2022-2023) Visualization](/assets/img/Poverty Rate Over Time by Race (Black vs. White).png)


#### 3. Predicted Jail Outcomes by State
I then examined predicted incarceration outcomes for children born between 1978 and 1983 whose parents were at the 25th percentile of national income. These predictions are based on census data and statistical modeling, incorporating privacy-protected estimates. 

Notable Findings:
- Highest combined Black/White incarceration rate: Hawaii (12.5%)
- Lowest combined rate: Rhode Island (1.8%)
- Highest Black incarceration rate: Nebraska (10.57%)
- Lowest Black incarceration rate: Rhode Island (1.6%)
- Highest White incarceration rate: Hawaii (2.5%)
- Lowest White incarceration rate: Rhode Island (0.2%)

Potential Errors: 
Predicted estimates: The incarceration rates are predicted outcomes based on statistical models using Census and ACS data for children born between 1978–1983 with parents at the 25th income percentile. These predictions, based on demographic and economic characteristics by Census tract, include privacy preserving noise and model assumptions rather than direct incarceration counts. 

Small population size effect: States like Hawaii and Nebraska have relatively small Black populations, which can distort percentage-based statistics and lead to unusually high predicted rates due to limited sample sizes.

### Predicted Jail Outcomes Black vs White by State (Children Born 1978–1983, Parents at 25th Income Percentile)
<head>
  <!-- Import Vega & Vega-Lite (does not have to be from CDN) -->
  <script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
  <!-- Import vega-embed -->
  <script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>
</head>

<div id="vis2"></div>
<script type="text/javascript">
  var spec = "https://raw.githubusercontent.com/siennacorreia/siennacorreia.github.io/refs/heads/master/assets/Predicted Jail Outcomes by Race and State (Children Born 1978–1983, Parents at 25th Income Percentile) (Alphabetical).json";
  vegaEmbed('#vis2', spec).then(function(result) {
    // Access the Vega view instance (https://vega.github.io/vega/docs/api/view/) as result.view
  }).catch(console.error);
</script>

### US Map Visualization: Predicted Jail Outcomes Black vs White (Children Born 1978–1983, Parents at 25th Income Percentile)
<head>
  <!-- Import Vega & Vega-Lite (does not have to be from CDN) -->
  <script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
  <!-- Import vega-embed -->
  <script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>
</head>

<div id="vis3"></div>
<script type="text/javascript">
  var spec = "https://raw.githubusercontent.com/siennacorreia/siennacorreia.github.io/refs/heads/master/assets/US Map Visualization: Predicted Jail Outcomes Black vs White (Children Born 1978–1983, Parents at 25th Income Percentile).json";
  vegaEmbed('#vis3', spec).then(function(result) {
    // Access the Vega view instance (https://vega.github.io/vega/docs/api/view/) as result.view
  }).catch(console.error);
</script>

##### 4. Mobility Metrics by Race, Gender, and Income 
Using U.S. Census data on children born between 1978-1983, I graphed four key outcomes by parent income percentile: wage rank, employment %, and jail %. These visuals reveal how mobility pathways are diverse across race and gender. One of the most surprising results was the sharp increase faced by Black males in the percentage of incarcerated children (the top left graph) in comparison to the Black female, White male, and White female. 

### 4 Graphs: Wage Rank, Employment %, College %, Incarceration %  
![4 Graphs on wage rank, employment %, college %, and incarceration %](/assets/img/Combined_Graphs.png)

##### 5. Simulation:
For my final visualization, I built a simulation in VS Code using Altair. It pulls from the same dataset used above, allowing the user to select a race, gender, and parent income percentile. Base on their inputs the model simulates:
- Jail outcome
- College attendance
- Employment at age 30
- Expected wage rank 
I initially designed it as a console input program, but for this post I created an interactive version with dropdown menus. 

Key Takeaways: 
- At the 100th percentile, the expected wage rank is $69.18 for White Americans vs $59.02 for Black Americans.
- At the 1st percentile, the jail probability for a Black male (21.2%) is nearly 20× higher than for a Black female (1.4%).
  
<head>
  <!-- Import Vega & Vega-Lite (does not have to be from CDN) -->
  <script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
  <!-- Import vega-embed -->
  <script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>
</head>

<div id="vis4"></div>
<script type="text/javascript">
  var spec = "https://raw.githubusercontent.com/siennacorreia/siennacorreia.github.io/refs/heads/master/assets/OutcomesSimulation.json";
  vegaEmbed('#vis4', spec).then(function(result) {
    // Access the Vega view instance (https://vega.github.io/vega/docs/api/view/) as result.view
  }).catch(console.error);
</script>

### User Input Simulation Outcome example
![1 outcome for the user input simulation](/assets/img/user_input.png)

# Discussion:
This project confirmed that racial disparities in mobility are persistent and systemic. Even when controlling for income, Black Americans, especially men, face elevated risks of incarceration and diminished access to college, stable employment, and high-earning jobs.
  Challenges that I faced during this process were finding reliable CSV data and merging datasets with differing formats, parsing long variable names into usable inputs for code visualization, and designing intuitive visualizations to tell a clear story. If I had more time, I would have furthered my project by researching historical context on why certain states have increased incarceration. Additionally, I would have expanded the simulation to include other races and maybe add explanations for each outcome.
