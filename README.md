## Project Overview:
With this project, I plan to analyze the evolution of the three-point shot in the NBA. Furthermore, I will examine how the increase in 3-point shots has impacted player metrics, including rebounding and positional roles.

## Data Retrieval:
Utilized NBA_API library to make API calls to the official NBA stats database. Collected data for players and teams from 1996-2025, utilizing a dataframe merge to combine player stats and player traits in Pandas to turn into a complete CSV.

## Planned Steps:
* Basic Analysis: I will find the regression line for 3PA and 3PM
* Volume and Efficiency: I will look into how overall FG% is affected by the increase in 3PA
* Analyzing 3PA by Position: I will look into 3PA and player position to analyze how player frames correlate with the increase in 3PA
* Rebounding Analysis: I will look into how 3PA affects rebounding numbers. I plan to test the hypothesis that more 3-pointers lead to an increase in rebounds for smaller players due to a larger bounce off the rim.

## Predictions:
* I expect to see a large jump in 3PA and 3PM over time
* I expect to see a decrease in overall FG%, but an increase in 3PT%
* I expect to see an evolution in the "stretch big", e.g., Dirk Nowitzki, bigger players who would once be expected to be interior players who were dominant from three
* I expect to see an increase in rebounding numbers for perimeter players, due to a larger bounce when shooting from distance

## Updates
* I have created a CSV table with many team stats that I may employ in a future project as well, but I will use it in this project to analyze 3PA, 3PM, team rebounding, FG%, and even blocks, as fewer interior shots should lead to fewer blocks
* CSVs have been created for team stats and player stats from 1996-2025
* Regression line has been plotted with observed values for 3PM and 3PA, and I have summarized key statistics as well, showing that Year is a great estimator for 3PM and 3PA
* Updated player stat creation, which was quite complicated due to physical features and stats being split in the API
* Next, I will do some cleaning and work 3PA by position and height over time
  * I am debating leaving out NAs or using imputation
  * I may fill unfilled positions by using the nearest mean height/weight
  * I may fill unfilled heights/weights by using the means for that position
  * I will probably exclude NAs that have multiple boxes unfilled

## Visualization and Analysis of 3PM and 3PA for team statistics from 1996-2025:
Judging the entire league's stats for a single season:
* For each year that passes, the expected value for 3-point attempts increases by 27.717
* For each year that passes, the expected value for 3-point makes increases by 10.124 
* The r^2 is high and the p-value is low for both the 3PM and 3PA statistics
* We would reject the null hypothesis that the year is not a significant predictor for both 3PM and 3PA, even when using a very small alpha like .001
* Year is a great estimator for both 3PM and 3PA

#### 3-point attempts vs Year Summary
* Slope:  27.717
* R-squared:  0.890
* P-value:  0.000000000000018
#### 3-point makes Vs Year Summary
* Slope:  10.124
* R-squared:  0.889
* P-value:  0.000000000000021
  
![Plot](https://github.com/nathankyryk/nba/blob/main/plots/nba_3pt_regression_plot.png)

## Visualization and Analysis of FG% and 3PT% for team statistics from 1996-2025:
* For each year that passes, the expected value for FG% increases 0.00084599
* For each year that passes, the expected value for 3PT% increases 0.00044823
* The R^2 values are not as high as the R^2 for attempts are
* We can confidently reject the null hypothesis that year is not a significant predictor for FG% using a small alpha, like .001
* We can reject the null hypothesis that year is not a significant predictor for 3PT% using an alpha of .01. Based on the p-value, there is almost 99.9% certainty that the year is significant.

#### FG Percent vs Year Summary
* Slope:  0.00084599
* R-squared:  0.584
* P-value:  0.000001
#### 3PT Percent Vs Year Summary
* Slope:  0.00044823
* R-squared:  0.314
* P-value:  0.001586

![Plot](https://github.com/nathankyryk/nba/blob/main/plots/nba_fg_percentages.png)

## Visualization of 3PA/game statistics for each position:
![Plot](https://github.com/nathankyryk/nba/blob/main/plots/avg_3pa_per_position_by_season.png)

## Visualization of REB/game statistics for each position:
![Plot](https://github.com/nathankyryk/nba/blob/main/plots/avg_rebounds_per_position_by_season.png)



## 
