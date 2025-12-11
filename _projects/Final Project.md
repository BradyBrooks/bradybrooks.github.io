---
name: Final Project 
tools: [Python, Altair, vega-lite]
image: assets/pngs/drug_overdose.png
description: U.S Deaths Breakdown
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Final Project: Breaking Down Deaths in the U.S


### By: Brady Brooks

## Plot 1: Naturally Caused Deaths in the U.S. with a Demograhic Breakdown

<vegachart schema-url="{{ site.baseurl }}/assets/json/natural_causes_dashboard.json" style="width: 100%"></vegachart>


## Description 1

#### Design Choices 

In this chart, I am visualizing the statics of the square footage of each building based on the year it was constructed. To do this, I used a line chart so the end user can compare the statistics overtime. Such as seeing if the average square footage has gone up each year. When creating the visualization I encoded the "Year Constructed" to a Temporal and the statistics to Quantitative. I also added an interactive dropdown menu that allows the user to select which statistic they would like to emphasize. The chart consists of 8 unique statistics and their uniquely colored line.The statistic options I made available are mean, min, 25%, 50%, 75%, and max. When one is selected that line is the only one that remains colored and the rest lose opacity and turn grey. This way the user can easily visualize the line they are trying to emphasize.

#### Data Transformation Discussion

There were many data transformations that I performed on this dataset. For starters, I made every instance that was 0 of Square Footage and Year Constructed equal to null. Afterwards, I grouped by Year Constructed and Square Footage so I could grab each Year's statistics. I also changed the Year Constructed column from int to datetime for easy visualization. Finally, I "melted" the dataframe and made it so each row contained a year constructed, one of the respective statistics, and its stat value. 

## Plot 2: Male vs Female Drug Overdoses by Age Group

<vegachart schema-url="{{ site.baseurl }}/assets/json/drug_overdose.json" style="width: 100%"></vegachart>


## Description 2

#### Design Choices 

In this chart, I am visualizing the statics of the square footage of each building based on the type of building. To do this, I used a bar chart so the end user can compare the statistics between types of buildings. When creating the visualization I encoded the "Usage Description" to a Nominal and the statistics to Quantitative. I also added an interactive dropdown menu that allows the user to select which statistic they would like to look at. The chart consists of 6 unique statistics and plots the user can pick from and the building types are uniquely colored bars. The statistic options I made available are mean, min, 25%, 50%, 75%, and max. When one is selected that plot is the only one that shows up. This way the user can easily visualize the building types and their statistics side by side.

#### Data Transformation Discussion

There were many data transformations that I performed on this dataset. For starters, I made every instance that was 0 of Square Footage equal to null. Afterwards, I grouped by Unique Description and Square Footage so I could grab each building type's statistics. Finally, I "melted" the dataframe and made it so each row contained a building type, one of the respective statistics, and its stat value.


## Plot 3: Male vs Female Drug Overdoses by Age Group

<vegachart schema-url="{{ site.baseurl }}/assets/json/unnatural.json" style="width: 100%"></vegachart>


## Description 2

#### Design Choices 

In this chart, I am visualizing the statics of the square footage of each building based on the type of building. To do this, I used a bar chart so the end user can compare the statistics between types of buildings. When creating the visualization I encoded the "Usage Description" to a Nominal and the statistics to Quantitative. I also added an interactive dropdown menu that allows the user to select which statistic they would like to look at. The chart consists of 6 unique statistics and plots the user can pick from and the building types are uniquely colored bars. The statistic options I made available are mean, min, 25%, 50%, 75%, and max. When one is selected that plot is the only one that shows up. This way the user can easily visualize the building types and their statistics side by side.

#### Data Transformation Discussion

There were many data transformations that I performed on this dataset. For starters, I made every instance that was 0 of Square Footage equal to null. Afterwards, I grouped by Unique Description and Square Footage so I could grab each building type's statistics. Finally, I "melted" the dataframe and made it so each row contained a building type, one of the respective statistics, and its stat value.


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://catalog.data.gov/dataset/monthly-provisional-counts-of-deaths-by-age-group-sex-and-race-ethnicity-for-select-causes" text="Dataset One - Total Deaths" %}
</div>


<div class="right">
{% include elements/button.html link="https://github.com/BradyBrooks/bradybrooks.github.io/blob/main/python_notebooks/Project%20for%20HW5.ipynb" text="The Analysis" %}
</div>

<div class="left">
{% include elements/button.html link="https://catalog.data.gov/dataset/drug-overdose-death-rates-by-drug-type-sex-age-race-and-hispanic-origin-united-states-3f72f" text="Dataset Two - Drug Overdoses" %}
</div>

<div class="right">
{% include elements/button.html link="https://altair-viz.github.io/index.html" text="Citation" %}
</div>