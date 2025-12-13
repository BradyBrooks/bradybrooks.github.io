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

The datasets used in this analysis are both sourced from data.gov and contain information on deaths within the United States. The primary dataset is titled “AH Monthly Provisional Counts of Deaths for Select Causes of Death by Sex, Age, and Race and Hispanic Origin.” Each observation represents a month between 2019 and 2021 and includes breakdowns by age group, sex, and race. The key metadata examined includes the total number of natural deaths and total deaths for each demographic group in that month.
The second dataset is titled “Drug overdose death rates, by drug type, sex, age, race, and Hispanic origin: United States.” Observations reflect the same demographic categories but are aggregated by year rather than by month, covering the period from 2010 to 2018. The primary metric in this dataset is the number of drug overdose deaths per 100,000 people.

Across both datasets, the analysis focuses on total deaths within each month or year, organized by demographic group.

## Plot 1: Naturally Caused Deaths in the U.S. with a Demograhic Breakdown

<vegachart schema-url="{{ site.baseurl }}/assets/json/natural_causes_dashboard.json" style="width: 100%"></vegachart>


## Description


In this chart, I am visualizing the breakdown of natural deaths in the US by demographics. The first chart, a heatmap, demonstrates the mean of the number of natural deaths per month split up by both age group, and gender. Each box is a shade of grey, based on how high or low the number of deaths is. When one of the boxes are selected, the bar chart on its right updates to futher break down the number of deaths by race. Each time a new box is selected, the bar plot updates showing the breakdown of race by age group and gender selected. Finally, the users are able to hover over bars and squares to see the exact amount of natural deaths for that specified age, gender, and race.

This chart was created by myself using Dataset 1 and Altair in the python notebook listed at the bottom of this page.

## Plot 2: Male vs Female Drug Overdoses by Age Group

<vegachart schema-url="{{ site.baseurl }}/assets/json/drug_overdose.json" style="width: 100%"></vegachart>


## Description 

In this chart, I am visualizing the breakdown of drug related deaths in America broken up by once again, age group and gender. The chart demonstrates a grouped bar chart displaying the number of drug related deaths, per 100,000 people, broken up by age group and the genders side by side.

This chart was created by myself using Dataset 2 and Altair in the python notebook listed at the bottom of this page.


## Plot 3: Male vs Female Drug Overdoses by Age Group

<vegachart schema-url="{{ site.baseurl }}/assets/json/unnatural.json" style="width: 100%"></vegachart>


## Description

In this chart, I am visualizing the breakdown of unnatural deaths in the US by demographics using a bar and tick plot. This plot is interactive as it allows the user to select either "Male" or "Female" to display its respective plot. The bars in this plot resemble the average number of unnatural deaths per year represented by hundreds, seperated by both gender and age group. The tick in this plot resemebles the average number of drug related deaths per year, also seperated by both gender and age group. This allows us to make a comparison between the number of drug related deaths to total unnatural deaths per year.

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
{% include elements/button.html link="https://altair-viz.github.io/index.html" text="Altair" %}
</div>