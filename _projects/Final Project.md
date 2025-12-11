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


## Description


In this chart, I am visualizing the breakdown of natural deaths in the US by demographics. The first chart, a heatmap, demonstrates the mean of number of natural deaths per month split up by both age group, and gender. Each box is a shade of grey, based on how high or low the number of deaths is. When one of the boxes are selected, the bar chart on its right updates to futher break down the number of deaths by race. Each time a new box is selected, the bar plot updates showing the breakdown of race by age group and gender selected. 

This chart was created by myself using Dataset 1 and Altair in the python notebook listed at the bottom of this page.

## Plot 2: Male vs Female Drug Overdoses by Age Group

<vegachart schema-url="{{ site.baseurl }}/assets/json/drug_overdose.json" style="width: 100%"></vegachart>


## Description 

In this chart, I am visualizing the breakdown of drug related deaths in America broken up by once again, age group and gender. The chart demonstrates a grouped bar chart displaying the number of drug related deaths, per 100,000 people, broken up by age group and the genders side by side.

This chart was created by myself using Dataset 2 and Altair in the python notebook listed at the bottom of this page.


## Plot 3: Male vs Female Drug Overdoses by Age Group

<vegachart schema-url="{{ site.baseurl }}/assets/json/unnatural.json" style="width: 100%"></vegachart>


## Description

#In this chart, I am visualizing the breakdown of unnatural deaths in the US by demographics using a bar and tick plot. This plot is interactive as it allows the user to select either "Male" or "Female" to display its respective plot. The bars in this plot resemble the average number of unnatural deaths per year represented by hundreds, seperated by both gender and age group. The tick in this plot resemebles the average number of drug related deaths per year, also seperated by both gender and age group. This allows us to make a comparison between the number of drug related deaths to total unnatural deaths per year.

This chart was created by myself using a merged version of Dataset 1, Dataset 2 and Altair in the python notebook listed at the bottom of this page.


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://catalog.data.gov/dataset/monthly-provisional-counts-of-deaths-by-age-group-sex-and-race-ethnicity-for-select-causes" text="Dataset One - Total Deaths" %}
</div>


<div class="right">
{% include elements/button.html link="https://github.com/BradyBrooks/bradybrooks.github.io/blob/main/python_notebooks/FinalProjectWorkbook.ipynb" text="The Analysis" %}
</div>

<div class="left">
{% include elements/button.html link="https://catalog.data.gov/dataset/drug-overdose-death-rates-by-drug-type-sex-age-race-and-hispanic-origin-united-states-3f72f" text="Dataset Two - Drug Overdoses" %}
</div>

<div class="right">
{% include elements/button.html link="https://altair-viz.github.io/index.html" text="Citation" %}
</div>