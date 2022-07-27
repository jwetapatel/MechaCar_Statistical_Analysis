# MechaCar_Statistical_Analysis

R Studio

Statistics and R

# Overview of the Project

In this project, We’ll help Jeremy and the data analytics team do the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings


# Resources

Softwares: RStudio v.1.4.1103, dplyr library v.1.0.3

Data sources : MechaCar_mpg.csv, Suspension_Coil.csv

# Linear Regression to Predict MPG

The MechaCar dataset contains a sample size of 50 prototypes measuring the miles per gallon across multiple variables. The linear regression was calculated using R in RStudio.

- Linear Regression

R script was applied to the dataset on several variables to get the following coefficients.

![CALL and Coefficients](https://user-images.githubusercontent.com/96400887/181066993-ec2dfd1e-2cb1-43c4-9765-95df0b1a1ee8.png)

# Summary of Linear Regression model

A summary of the linear regression can be displayed to determine the quality of the dataset. In this distribution of the residuals, the dataset fits in with the normal parameters, where the absolute value of the min and max are comparable |-19.47|~|18.58| and the median -.07 is close to zero.

<img width="592" alt="2_sum_stat" src="https://user-images.githubusercontent.com/96400887/181067223-90bb598d-e394-4aa7-bc2e-525731ef0cee.png">


A 95% level of confidence was predetermined, meaning the p-value should be compared to alpha = .05 level of significance to verify if statistically significant.
Coefficients:

In summary, vehicle length and ground clearance variables represent non-random amounts of variance as applied to the mpg values.

The multiple linear regression formula for mpg = -.01 + 6.267(vehicle length)+.001(vehicle weight)+.069(spoiler angle)+3.546(ground clearance)-3.411(AWD), which results in a non-zero slope.

R-squared is .7149, which is a strong correlation for the dataset and shows the dataset is an effective dataset. However, r-squared is not the only consideration for effectiveness. There may be other variables not included in the dataset contributing to the variation in the mpg.

# Summary Statistics on Suspension Coils

- Manufacturing Lot Summary

Below is the summary statistics of all of the manufacturing lots. The mean is 1498.78 for this sample and the population mean was determined to be 1500.

![total_summary table](https://user-images.githubusercontent.com/96400887/181067397-a161e011-7af6-4385-88a9-21a6bb207118.png)

- Summary by Manufacturing Lot Number

The means of the lot numbers are similar to the population mean and the sample mean

![lot_summary table](https://user-images.githubusercontent.com/96400887/181067450-eddd29ec-2694-4eb7-913a-219c65ce2794.png)

In the total summary, we can see the variance of all three lots in tandem does fall under the maximum variance of 100 PSI with a variance of 62 PSI.

In the lot summary, we see that the major contributor to the variance is lot 3 with a variance of 170 PSI with the other two lots having variances below 8 PSI.

In total, the manufacturing data meets the maximum variance in PSI requirement, but we can see that there are clearly big problems in lot 3 with a variance of 170 PSI. Lot 3 does not meet the maximum variance requirement.

# T-Tests on Suspension Coils

- T-test for all Lots

All Manufacturing Lots: p-value = .6028, alpha = .05
.60 > .05, which means the total manufacturing lot is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

![data_Deliverable 3](https://user-images.githubusercontent.com/96400887/181067648-6f9cda86-57c2-4685-9d53-8ec951dbaa5b.png)

- T-test for Lot 1

Lot 1: p-value = 1, alpha = .05
1 > .05, which means Lot 1 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

![lot 1 test](https://user-images.githubusercontent.com/96400887/181067712-617ae0a4-f606-45f6-a16b-4b930e91a7f0.png)

- T-test for Lot 2

Lot 2: p-value = .6072, alpha = .05

.60 > .05, which means Lot 2 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

![lot 2 test](https://user-images.githubusercontent.com/96400887/181067759-ad67f111-4e18-4307-8807-b5703908bf43.png)

- T-test for Lot 3

Lot 3: p-value = .04168, alpha = .05
.04 < .05, which means it is statistically significant from the normal distribution and normality cannot be assumed. However, the mean falls within the 95% confidence interval.

![lot 3 test](https://user-images.githubusercontent.com/96400887/181067844-fdbfd086-9fff-4f9e-a88e-c5a1dc5f0dcb.png)

The overall manufacturing, Lot 1, and Lot 2 show a normal distribution. Therefore, there is not sufficient evidence to reject the null hypothesis, which shows the two means are statistically similar.

# Study Design: MechaCar vs Competition

In order to compare the performance of the MechaCar against the competition, we need to address a few observables which would be of interest to our customers. These variables will be cost, city and highway fuel efficiency, horsepower, safety rating, and carbon waste output.

1. What metric or metrics are you going to test?

  The next metrics to test should be the safety rating, horsepower, and highway fuel efficiency, which address some safety concerns of consumers.

2. What is the null hypothesis or alternative hypothesis?

  We can make a null hypothesis stating that it is not different from the competition and our Alternative would be the opposite
  The alternative hypothesis is that the mean of the safety rating is not zero.

3. What statistical test would you use to test the hypothesis? And why?

  We will perform one-tailed t-tests in order to determine if the MechaCar has higher or lower observed values in these variables than the competition according to      which direction the consumer would prefer. 

4. What data is needed to run the statistical test?

 We need these statistical tests, including the cost, fuel efficiency, horsepower, safety rating, and carbon waste output data from the MechaCar as well as the MechaCar's competitors.





















