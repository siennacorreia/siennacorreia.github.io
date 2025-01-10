---
layout: post
title: Dataset Analysis Lab #3 Report
subtitle: Student Lifestyle Dataset statistical analysis 
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/student.jpg
share-img: /assets/img/path.jpg
tags: 
author: Sienna Correia
---

## Dataset Info:
I worked with the Student Lifestyle Dataset from Kaggle, with data on "Daily Lifestyle and Academic Performance of Students."
link: https://www.kaggle.com/datasets/steve1215rogg/student-lifestyle-dataset 

Upon looking into the dataset, I am most interested in the stress level relatonship to GPA and study hours per day. My initial hopes in analyzing the dataset were to understand the effect that daily study hours and GPA had on stress levels among college students.

## Dataset Analysis:

### Visualizations of the dataset - Violin Plots 

![Stress Levels vs GPA Violin Plot](/assets/img/stress_vs_gpa.png)
 
![Stress Levels vs Daily Study Hours Violin Plot](/assets/img/stress_vs_study_hours.png)


### Variables Examined
Stress_Level: Categorical variable with three levels — Low, Moderate, and High.
GPA: Variable indicating academic performance.
Study_Hours_Per_Day: Variable showing daily time spent on studying.

### Additional lifestyle variables include:
Extracurricular_Hours_Per_Day
Sleep_Hours_Per_Day
Social_Hours_Per_Day
Physical_Activity_Hours_Per_Day

### Distributions of variables 

> #### Mean and Median GPA by Stress Level:
>  Stress_Level : mean : median : std                
>
> High :
> 3.261973   :   3.27   :   0.274960
>
> Low :
> 2.816869   :   2.82   :   0.215396
>
> Moderate :
> 3.024837   :   3.02   :   0.220653

> #### Mean and Median Study Hours by Stress Level:
>  Stress_Level : mean : median : std
> 
> High :
> 8.385034   :    8.7   :    1.238311
>
> Low :
> 5.474411   :    5.5   :    0.279753
>
> Moderate :
>  6.969585   :   7.0   :    0.597576

#### GPA
Center: The mean and median GPA indicate a general trend of satisfactory academic performance.

Variability: GPA shows moderate variability, with a tighter spread in the "Moderate" stress group compared to "Low" and "High".

#### Study Hours Per Day 
Center: Students generally study for about 5–7 hours daily, with the "High" stress group showing higher averages.

Variability: Study hours exhibit greater variability in the "High" stress group, suggesting a mix of overstudying and / or avoidance behaviors.

### Relationships between variables
GPA vs Stress Level:
Positive relationship observed: Higher stress levels correlate with higher GPA. Students in the "High" stress group show improved academic performance, potentially due to increased motivation or effort.

Study Hours vs Stress Level:
Positive relationship: Students in the "High" stress group spend more time studying, suggesting a link between stress and effort.


### Limitations of your analysis and the dataset
Dataset Quality:
Potential selection bias: High achievers might be overrepresented, skewing the relationship between stress and GPA.
Missing variables: Factors like mental health or access to resources are unaccounted for.

Causation vs Correlation:
Observed relationships (e.g., stress correlating with GPA) may not imply causation. External factors like personal discipline or institutional expectations might drive these results.

Categorical Simplification:
Stress level categorization (Low, Moderate, High) may oversimplify nuanced stress experiences.

## Conclusions:
Stress and Academic Performance:
Students with higher stress levels tend to achieve higher GPAs.
Supporting evidence: Violin plot distributions show a clear trend of increasing GPA with stress.

Stress and Study Effort:
Higher stress correlates with longer study hours.
Supporting evidence: "High" stress students spend more time studying, as shown in the violin plot.

Implications:
While high stress may drive academic performance, prolonged exposure could negatively affect other areas like sleep or mental health.
A balanced approach to managing stress is crucial for sustained performance and well-being!
