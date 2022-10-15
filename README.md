# MechaCar Statistical Analysis

Using R and Statistics to analyze car data

## Overview of Project

Information about production data on a car prototype. Statistics created using R. 

### Purpose

AutosRUs has created a prototype, the MechaCar, which is having some production troubles that are blocking the manufacturing team's progress. Analysis of production data for insights such as:
- Multiple linear regression analysis to predict mpg
- Summary statistics on pounds per square inch (PSI) of suspension coils
- Running t-tests on manufacturing lots of coils
- A statistical study to compare vehicle performance

## Results

## Linear Regression to Predict MPG

#### *Linear Regression Model*
![linear-regression-mpg](https://user-images.githubusercontent.com/108373151/196009304-20278b1f-af79-48c7-ab27-c0856f18e494.jpg)

#### *Linear Regression Model Summary*
![linear-regression-mpg-summary](https://user-images.githubusercontent.com/108373151/196009309-f4998d6b-1028-41de-b8e5-c65d2a6b7e1b.jpg)

In the above snapshots, the individual variables or coefficients' p-values (Pr(>|t|)) are as follows:
- Vehicle Length: 2.60e-12
- Vehicle Weight: 0.0776
- Spoiler Angle: 0.3069
- Ground Clearance: 5.21e-08
- AWD: 0.1852

Additional information gathered from the linear regression model:
Multiple R-squared: 0.7149
Overall p-value: 5.35e-11

#### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

From the dataset, it is possible to predict that the variables/coefficients which provided a non-random amount of variance to the mpg values are: vehicle weight (0.0776), spoiler angle (0.3069) and AWD (0.1852).

#### Is the slope of the linear model considered to be zero? Why or why not?

The slope of our analysis is 5.35e-11 which is much smaller than our assumed significance level of 0.05. There is sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.

#### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

The multiple R-squared value is 0.7149 which means that about 71.5% of the variability of our dependent variable is explained using this linear model. The higher the value of the R-squared, the more that the variables can be explained or predicted using this linear model.

## Summary Statistics on Suspension Coils

#### *Total Summary Statistics*
![total-summary](https://user-images.githubusercontent.com/108373151/196010404-e6fb1717-10e8-4317-885f-df229a6874cd.jpg)

#### *Summary Statistics by Lot*
![lot-summary](https://user-images.githubusercontent.com/108373151/196010414-f27bee69-bab7-49bf-a5bc-57bf8e81ea90.jpg)

#### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

Referring to the images above, overall, the variance of the suspension coils (62.29) does not exceed 100 pounds per square inch (PSI), so as a whole, the data meets the design specifications. However, if you drill down to each lot, it is clear that while lots 1 and 2 variances have less than 100 PSI, lot 3's variance is over 170 PSI. This lot would fail the design specifications.

## T-Tests on Suspension Coils

#### *Overall T-Test Results*
![t-test-overall](https://user-images.githubusercontent.com/108373151/196010666-fb8fb3ae-e202-4315-844b-3f8c22e5daaf.jpg)

#### *T-Test Results Lot 1*
![t-test-lot1](https://user-images.githubusercontent.com/108373151/196010620-3c3f2fcf-de05-4680-9292-dc18a219c066.jpg)

#### *T-Test Results Lot 2*
![t-test-lot2](https://user-images.githubusercontent.com/108373151/196010626-7a72533e-cc00-4c26-a91a-ef5596618791.jpg)

#### *T-Test Results Lot 3*
![t-test-lot3](https://user-images.githubusercontent.com/108373151/196010632-a3ea9989-6d8e-49e2-a4d8-3a3750dbf639.jpg)

In the above snapshots, the p-values are as follows:
Overall: 0.06028
Lot 1: 1.00
Lot 2: 0.6072
Lot 3: 0.04168

Across all manufacturing lots, with a p-value of 0.06028 the PSI is was not below the common 0.05 significance level. Therefore, the PSI across all manufacturing lots in statistically similar from the population mean of 1,500 pounds per square inch. There is not sufficient evidence to reject the null hypothesis.

Likewise, Lot 1 with a p-value of 1.00 and Lot 2 with a p-value of 0.6072 are statistically similar. However, Lot 3 with a p-value of 0.04168 is below the 0.05 significance level. So the PSI in lot 3 is statistically different than the population mean of 1,500 pounds per square inch.

## Study Design: MechaCar vs Competition

With gas prices still high, inflation increases, and safety in mind, consumers who are interested in the MechaCar will be interested in:
1) How the MechaCar performs in miles per gallon (mpg) to its competition in both city and highway metrics
2) The price of MechaCar compared to the competition
3) The safety rating of MechaCar compared to its competitors

The following hypotheses will be taken into account:
1) H0: There is no statistical difference in mpg between MechaCar and its competitors
Ha: MechaCar's mean mpg is statistically different than the mean of the competitor's mpg
2) H0: There is no statistical difference in price between MechaCar and its competitors
Ha: MechaCar's price is statistically different than the mean of the competitor's price
3) H0: There is no statistical difference in the safety rating between MechaCar and its competitors
Ha: MechaCar's safety rating is statistically different than competitor's safety rating

To test the hypotheses, data from similar make and model cars from competitors will need to be gathered. Similar models will be evaluated in car class, weight, length, etc. across all manufacturing companies to find the most similar models for comparison. While this will limit the data obtained, this analysis will provide the best gauge of whether MechaCar truly outperforms the competition in the ways that matter to the consumers.

Ideas for comparison and visualization would be:
1) Box and whisker plots to compare MechaCar's mpg against competitors, faceted in both highway and city mpg for easy comparison
2) A scatter plot to compare MechaCar's price with the other value points being the competitor prices
3) A T-Test to determine how statistically different the safety rating of MechaCar is compared to similar cars