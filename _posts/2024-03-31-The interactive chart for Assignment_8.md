---
layout: post
title: The interactive chart for Assignment_8
tags: [Technology, Blogging]
description: This is a blog post for IS 445 assignment.
---

{% include assignment.html %}

## Analysis of chart

### In assignment 7, I did a line chart about trends in the average number of floors in buildings constructed since the year 2000, grouped by their usage description. In this assignment, I tried to combine the change of average floors with the distribution of square footage and group them by usage description. 

### Scatter Chart

This scatter plot visualizes the relationship between the construction year and square footage of buildings constructed from 2001 to 2020. In terms of design choices, I used a quantitative x-axis to represent the "Year Constructed" with a domain range limited between 2000 and 2020 to ensure only data from the 21st century is displayed. The y-axis is quantitative, showing "Square Footage" to illustrate the size of the buildings. Color encoding is based on user click selection, highlighting the selected "Usage Description" using Altair's tableau20 color scheme. This scheme was chosen because it provides a wide range of colors for differentiating various usage descriptions effectively. The choice of color aims to highlight the usage of buildings distinctly, making the categorization more intuitive to the observer.

### Bar Chart

The bar chart focuses on the average number of floors of buildings constructed each year from 2001 to 2020. Here, I utilized an ordinal x-axis to represent "Year Constructed," with axis labels angled at 45 degrees to improve readability. The y-axis is quantitative and displays the average "Total Floors". Color encoding responds to user click actions, turning the bars to "lightgray" when selected and "steelblue" when not. This color design is meant to clearly differentiate the data of interest in an interactive selection context.

### Interactive

In terms of interactivity, I chose click selection as the primary interactive feature. Users can click on points within the scatter plot to filter the data in the bar chart, only displaying average floor information for buildings constructed in the selected years. This design allows users to focus on specific use of buildings for deeper insights. The choice of interactivity aims to make the visualization clearer and more engaging, providing users with an intuitive way to explore and understand the changes in building characteristics in the early 21st century.
﻿
Data transformations were carried out in the Python notebook using pd.read_csv to read the data, applying filters to exclude records with a year of 0, square footage of 0, or number of floors of 0. Moreover, only buildings constructed from 2001 onwards were selected for display. These transformations ensure the accuracy of analysis and visualization, focusing on building trends in the 21st century.

The Data：[Data Link](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)
The Notebook：[Link to Jupyter Notebook](https://github.com/modestcharlie/IS445_Assignment8/blob/main/_notebooks/Assignment_8.ipynb)