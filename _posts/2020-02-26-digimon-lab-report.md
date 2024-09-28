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
2. For task two, I created list to hold all data in the file. Then I created a function to check and count up for each digimon that had the value for the attribute being checked. Finally I made an if statement that could be modified for any value and attribute, which assigned values to the variables `value` and `attribute`, and printed the number of Digimon for an attribute with that value.    
3. In order to accomplish task 3, I attempted to make teams of 1-3 Digimon, then called the `make_team` function to check if the combinations of Digimon met the criteria, and printed the `team_names`, `total_memory`, and "total_attack`.

## Steps that Worked
Task 1: First, I created an empty `total_HP` list, then I added all HP values from the file, next I used that value to find the average HP value by dividing the sum of the `total_HP` by the length of the `total_HP`, and finally I printed the `avg_HP` value.

(entire task 1 code)
>        import csv
> 
>       with open("datasets/digimon.csv", "r") as f:
> 
>        data = csv.DictReader(f)
>        total_HP = []   
>        for row in data:
> 
>            total_HP.append(float(row["HP"]))
>       
>      avg_HP = sum(total_HP) / len(total_HP)
> 
>      print(f"1. The total HP for all digimon is: {avg_HP}")

Task 2: First, I started with creating an empty `species_data` list with all rows from the data dictionary. I then created a `count` variable and counted the total digimon in stage baby. This was a very narrowly focused code, so to generalize it for any attribute, I still had an empty list, however, created a function to  increase `count` if the attribute corresponded to the value.

(generalized function code)
>      def count_digimon_attribute(species_data, attribute, value):
>
>      count = 0
>
>      for row in species_data:
>          # Check for the attribute
>
>          if row[attribute] == value:
>              count += 1
>
>      return count

Task 3: 

(nested for loop 3 code)
>    elif n == 3: # team size is 3 (same idea as adding 2, another nested for loop)
>       for element in range(len(data)):
>          for element2 in range(element + 1, len(data)):
>              for element3 in range(element2 + 1, len(data)):
>                  team = [data[element], data[element2], data[element3]]
>                  if is_valid(team):
>                      return team


## Challenges
1. For task 1, I did not face many challenges, and identified one small indentation error!
2. The biggest challenege I faced in completing task 2 was determining how to generalize the code to check for and count any attribute and value. 
3. In my efforts to fulfill task 3, the largest obstacle I overcame was making a team of exactly three digimon with exactly 15 memory because this combination required nested for loops to make sure each digimon met the requirements before being added to the team. 


## Skills Learned
Overall, through this first lab and reflection post, I gained more comfort in using dictionaries, lists, functions, and nested for loops in python! I also enjoyed using markdown to make this a **presentable** and **appealing** reflection post!
