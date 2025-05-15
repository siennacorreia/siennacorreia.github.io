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
As my final project I decided to research the mobility barriers for Black Americans, especially focused on incarceration and then also economic disparities including education, employment, and wage. In my project, I sought to narrow in on and explore the inequality between Black and White American counterparts. 

Hypothesis: The economic and educational barriers to mobility are higher for Black American children versus their White counterparts and persists even at higher income levels. 

# Data:

I initially found the number of incarcerated individuals by Race during 1978 to 2011. 

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

### Poverty Rate Over Time by Race (Black vs. White) (2022-2023)
![Poverty Rate Over Time by Race (Black vs. White) (2022-2023) Visualization](/assets/img/Poverty Rate Over Time by Race (Black vs. White).png)

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
  var spec = "https://raw.githubusercontent.com/siennacorreia/siennacorreia.github.io/refs/heads/master/assets/assets/US Map Visualization: Predicted Jail Outcomes Black vs White (Children Born 1978–1983, Parents at 25th Income Percentile).json";
  vegaEmbed('#vis3', spec).then(function(result) {
    // Access the Vega view instance (https://vega.github.io/vega/docs/api/view/) as result.view
  }).catch(console.error);
</script>

# Discussion:


# Still Need to Do...
- Clearly align my definition of mobility barriers
- make the simulation insteractive in a way on the web
- make this post more fleshed out to show all steps of the process! ... Deciding on topic, research, finding csvs and other data, cleaning the data, making all graphs, making simulation, challenges along the way, how I would have furthered my work if more time
