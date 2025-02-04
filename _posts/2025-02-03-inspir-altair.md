---
layout: post
title: Inspir Altair Cool Visualizations!
subtitle: Women in Songwriting & Ivy League Women's Soccer Standings
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/visualizations.png
share-img: /assets/img/path.jpg
tags: 
author: Sienna Correia
---
## Original Visualizations:
![Pudding Ivy League Women's Soccer Standings 2009-2024 Visualization](/assets/img/original_standings.png)

![Reddit Women in Songwriting Visualization](/assets/img/original_song.png)

## Recreations of Visualizations:

### Recreation of the Ivy League Women's Soccer Standings 2009-2024 Visualization

<head>
  <!-- Import Vega & Vega-Lite (does not have to be from CDN) -->
  <script src="https://cdn.jsdelivr.net/npm/vega@[4]"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-lite@[5]"></script>
  <!-- Import vega-embed -->
  <script src="https://cdn.jsdelivr.net/npm/vega-embed@[6]"></script>
</head>
<body>

<div id="vis"></div>

<script type="text/javascript">
  var spec = "[https://raw.githubusercontent.com/vega/vega/master/docs/examples/bar-chart.vg.json](https://raw.githubusercontent.com/siennacorreia/siennacorreia.github.io/refs/heads/master/assets/women_in_songwriting.json)";
  vegaEmbed('#vis', spec).then(function(result) {
    // Access the Vega view instance (https://vega.github.io/vega/docs/api/view/) as result.view
  }).catch(console.error);
</script>
</body>


#### Description:
This line chart with labels and points represents the rankings of Ivy League women’s soccer teams from 2009 to 2024. Each colored line represents a team, with its placement on the y-axis indicating its rank for that year. The y-axis is reversed so that 1st place appears at the top, and 8th place at the bottom. A gap is left for 2020, when the season was disrupted.

##### The code used to generate the line chart & legend:
>     lines = alt.Chart(df_long).mark_line(size=2).encode(
>         x=alt.X('year:O', title="Year", axis=alt.Axis(labelAngle=-45)),
>         y=alt.Y('rank:Q', title="Place", axis=alt.Axis(labelAngle=0, values=list(range(1, 9)))), 
> 
>         color=alt.Color('team:N', 
>         scale=color_scale, 
>         legend=alt.Legend(title="Teams", orient="left")  
>    )

#### Interest:
It clearly visualizes trends in team performance over time, showing how some teams improve while others struggle. The visual complexity of the crisscrossing lines makes it engaging while still being readable. I enjoyed using the `tooltip` feature, so that when the user hovers over a point the tooltip displays year, team, and place ranked for that year. I chose this visualization because it effectively communicates historical patterns in sports rankings, allowing for easy comparison between teams.

##### The code used to organize each team by various colors:
>     team_colors = {
>         'Harvard': '#007bff', 'Dartmouth': '#dc3545', 'Brown': '#ffc107',
>         'Yale': '#28a745', 'Cornell': '#000000', 'Princeton': '#17a2b8',
>         'Columbia': '#fd7e14', 'UPenn': '#6f42c1'
>     }
> 
>     color_scale = alt.Scale(domain=list(team_colors.keys()), range=list(team_colors.values()))


#### Marks & Channels:
Marks: 
- line (used to connect rankings for each team over time)
- circle (used at each rank to highlight positions)
- text (used to display ranking numbers directly on points)

Channels:
- x-axis → Year (ordinal scale)
- y-axis → Rank (quantitative scale, reversed so 1 is at the top)
- color → Team (nominal scale)
- text → Shows ranking values at each point

#### Challenges:
I did not face many larger challenges in recreating the original Ivy League Women's Soccer Standings visualization. However, there are slight minor inaccuracies in my replication compared to the original visualization, including spacing and outlining the numbers in white. 

### Recreation of the Women in Songwriting Visualization
![Recreation of the Women in Songwriting Visualization](/assets/img/women_in_songwriting.png)
#### Description:
This stacked bar chart visualizes the gender distribution of songwriters for top 5 Billboard hits over time (1958-2022).
Each bar represents a year and is stacked by gender categories:
Purple: Male songwriters
Yellow: Female songwriters
Red: Non-binary songwriters
Gray: Unknown gender
The total height of each bar represents the total songwriting credits for that year.

##### The code used to generate the stacked bar chart:
>     chart = alt.Chart(merged_data).mark_bar(size=4).encode(
> 
>       x=alt.X('year:O', title="Year", axis=alt.Axis(labelAngle=-45, values=[y for y in range(1958, 2023, 5)])), 
>
>       y=alt.Y('count:Q', title="Total Songwriters", stack=True), 
>
>       color=alt.Color('gender:N', scale=color_scale, legend=alt.Legend(title="Songwriter Representation", orient='bottom')),
>
>       tooltip=['year', 'gender', 'count'] 
>
>     ).properties(
>         width=900,
>         height=500
>     )

#### Interest:
It highlights gender disparities in the music industry, showing how male songwriters have historically dominated. The annotations effectively tell a story, drawing attention to specific historical moments. The use of color makes the patterns clear, while the stacked bars allow us to compare trends over time. I enjoyed using the `tooltip` feature, so that when the user hovers over a bar the tooltip displays year, gender category, and count of songs for that year. I chose this visualization because it presents an important social issue in a way that is both visually compelling and informative.

##### The code used to add annoations to the right of the stacked bar chart: 
>     annotations = alt.Chart(pd.DataFrame({
>
>       'count': [3, 192, 50], 
>
>       'Text': ["Women had 33 songwriting credits for top 5 hits in 2022.",
>              "Men had 192 songwriting credits for top 5 hits in 2022.",
>              "3 songwriting credits went to non-binary writers in 2022."]
>
>     })).mark_text(
>
>       align='left', dx=10, dy=0, color='white', fontSize=12
>
>     ).encode(
>
>       x=alt.value(900),  # Text on the right
>
>       y='count:Q',
>
>       text='Text'
>     )

#### Marks & Channels:
Marks:
- bar (used for stacked bars representing songwriter counts)
- text (used for annotations and labels)

Channels:
- x-axis → Year (ordinal scale)
- y-axis → Total songwriter count (quantitative scale)
- color → Gender category (nominal scale)
- text → Highlights key insights (annotations on the chart)

#### Challenges:
In my replication, women's contributions (yellow bars) appear at the bottom, while in the original, they are at the top. This was a challeneged I faced in replicating the original, as the y-axis is total songwriters in each group. This made it so the number of songwriters per group aligned with its location in the bar chart, placing men at the top instead of women.
Another challenge I faced recreating the aspect of the original where each bar is composed of tiny horizontal segments, where each segment represents one song in that category. My version stacks entire gender groups together, rather than individual songs being separate segments.
