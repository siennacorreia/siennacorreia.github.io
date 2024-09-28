---
layout: post
title: Digimon Lab #1 Report
subtitle: Reflection of My Process!
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/Digimon.png
share-img: /assets/img/path.jpg
tags: 
author: Sienna Correia
---

## Tasks:
1. Find the average HP of all Digimon
2. Write a function that can count the number of Digimon with a specific attribute
3. If your Digimon team only has 15 Memory, name a team of up to 3 Digimon that has at least 300 attack (Atk) in total

(each of the discussion sections are divided into three bullet points, each corresponding to the task being discussed) 

## Methods
1. For completing task one, I chose to create a list to hold all HP values found in the Digimon csv file. 

## Steps that Worked
1. First, I created an empty `total_HP` list, then I added all HP values from the file, next I used that value to find the average HP value by dividing the sum of the `total_HP` by the length of the `total_HP`, and finally I printed the `avg_HP` value.

<`import csv

with open("datasets/digimon.csv", "r") as f:
   data = csv.DictReader(f)
   total_HP = []
   
   for row in data:
       total_HP.append(float(row["HP"]))
       
avg_HP = sum(total_HP) / len(total_HP)
print(f"1. The total HP for all digimon is: {avg_HP}")`

## Challenges
what could have gone better

## Skills Learned
what you learned during this lab 
screenshots, pseudocode, etc to elaborate on your response!
