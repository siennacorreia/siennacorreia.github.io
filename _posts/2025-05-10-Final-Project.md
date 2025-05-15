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

## Tasks:
### Recreation of the Ivy League Women's Soccer Standings 2009-2024 Visualization

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
