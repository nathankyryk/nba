---
layout: post
author: Nathan Kyryk
title: 3-Pointer Evolution in the NBA
---
## Project Overview:
With this project, I plan to analyze the evolution of the three-point shot in the NBA. Furthermore, I will examine how the increase in 3-point shots has impacted player metrics, including rebounding and positional roles.

## Data Retrieval:
I will utilize the NBA_api package in Python to retrieve league-wide NBA stats. I will use data from 1996 to the present.

## Planned Steps:
* Basic Analysis: I will find the regression line for 3PA and 3PM
* Volume and Efficiency: I will look into how overall FG% is affected by the increase in 3PA
* Clustering by Frame: I will look into 3PA, height, weight, and position to analyze how player frames correlate with the increase in 3PA
* Rebounding Analysis: I will look into how 3PA affects rebounding numbers. I plan to test the hypothesis that more 3-pointers lead to an increase in rebounds for smaller players due to a larger bounce off the rim.

## Predictions:
* I expect to see a large jump in 3PA and 3PM over time
* I expect to see a decrease in overall FG%, but an increase in 3PT%
* I expect to see an evolution in the "stretch big", e.g., Dirk Nowitzki, bigger players who would once be expected to be interior players who were dominant from three
* I expect to see an increase in rebounding numbers for perimeter players, due to a larger bounce when shooting from distance

## Updates
* I have created a CSV table with many team stats that I may employ in a future project as well, but I will use it in this project to analyze 3PA, 3PM, team rebounding, FG%, and even blocks, as fewer interior shots should lead to fewer blocks
* I still need to create a CSV containing individual player or positional statistics
  * If doing individual players, I will likely do scraping on a site like Basketball Reference and filter out players averaging below 19 minutes or so, as there is a large amount of data
  * I will likely take positional stats over the years
