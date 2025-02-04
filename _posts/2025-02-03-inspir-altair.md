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
![Recreation of Ivy League Women's Soccer Standings 2009-2024 Visualization](/assets/img/soccer_standings.png)
#### Description:
This line chart with labels and points represents the rankings of Ivy League women’s soccer teams from 2009 to 2024. Each colored line represents a team, with its placement on the y-axis indicating its rank for that year. The y-axis is reversed so that 1st place appears at the top, and 8th place at the bottom. A gap is left for 2020, when the season was disrupted.
#### Interest:
It clearly visualizes trends in team performance over time, showing how some teams improve while others struggle. The visual complexity of the crisscrossing lines makes it engaging while still being readable. I chose this visualization because it effectively communicates historical patterns in sports rankings, allowing for easy comparison between teams.
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


![Recreation Women in Songwriting Visualization](/assets/img/women_in_songwriting.png)
#### Description:
This stacked bar chart visualizes the gender distribution of songwriters for top 5 Billboard hits over time (1958-2022).
Each bar represents a year and is stacked by gender categories:
Purple: Male songwriters
Yellow: Female songwriters
Red: Non-binary songwriters
Gray: Unknown gender
The total height of each bar represents the total songwriting credits for that year.

#### Interest:
It highlights gender disparities in the music industry, showing how male songwriters have historically dominated. The annotations effectively tell a story, drawing attention to specific historical moments. The use of color makes the patterns clear, while the stacked bars allow us to compare trends over time. I chose this visualization because it presents an important social issue in a way that is both visually compelling and informative.
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
