# MechaCar Statistical Analysis using R

The purpose of the challenge was to apply statistical analysis using the programming language "R" to provide insight on production data for an auto company.

## Linear Regression to Predict MPG (Deliverable 1)
Summary: After reading in the `MechaCar_mpg.csv` file, the lm() function is used to pass in all six variables (columns from the dataset) to determine their coefficients. 
The function is used for building linear models, in which it takes in two main arguements 1. Formula 2. Data. Here in the function, the "Formula" is predicting the dependent variable(mpg) by adding the 5 other variables of interest (our independent variables), whereas the "Data" is the dataframe created when we brought in the csv file. 

### Multiple Linear Regression Model 
![](resources/Deliverable_1a.PNG)

### Multiple Linear Regression Model Summary
In order to run the summary of the regression model to ensure it's statistically signficant, there are two options to run it (both using the summary() function).
First, you can just pass the lm() formula we wrote as is through the summary () function -or- assign the lm() formula a variable and pass that variable through the summary() funtion. Either way, the results are the same.
![](resources/Deliverable_1b.PNG)
![](resources/Deliverable_1c.PNG)

<i>Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?</i><br>
Looking at the p-values of each coefficient, we can see that vehicle_length and ground_clearance(as well as intercept) are unlikely to provide random amounts of variance
to the linear model. This means that these variables have a significant impact on mpg. In addition, because the intercept is significant, there are other variables that
contribute to the variation that have not been included in the model. 

<i>Is the slope of the linear model considered to be zero? Why or why not?</i><br>
Despite the estimate coefficients being extremely close to zero, it's inaccurate to claim that the slope is in fact zero. 
In addition, the p-value of 5.35e-11 states that there is a significant relationship, meaning then that the slope will not be equal to zero.
The null hypothesis states that the slope is equal to zero, and with this significance level, we are rejecting the null. 

<i>Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?</i><br>
Based on the R2(R-squared) value of 0.7149, it means that 71% of the variance measuring mpg can be predicted by the variables taken into account. However, to adjust for variables with a weaker association, by looking at the Adjusted R-squared, we can state that the prediction model is 68.25% effective.

---

## Summary Statistics on Suspension Coils (Deliverable 2)

"In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots." Using R, the following summary statistics table show: <br> 
(1) The suspension coil’s PSI continuous variable across all manufacturing lots<br>
![](resources/Deliverable_2a.PNG)<br>
(2) The following PSI metrics for each lot: mean, median, variance, and standard deviation.<br>
![](resources/Deliverable_2b.PNG) <br>

<i>The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?</i><br>
Based on the requirements and the summaries provided, we can see that across all manufacturing lots, together they meet the design specifications. 
As noted in the variance, the 62.29 PSI does not exceed the 100 PSI specification. Looking at the breakdown summary of each lot, we see that Lot 1 and Lot 2 meet the specifications. Lot 1 has a PSI of 0.98 while Lot 2 shows a 7.47 PSI, well below the 100 PSI requirement. Unfortunately, the summary shows Lot 3 does not meet the specification, but rather exceeds it with a 170.29 PSI.

---

## T-Tests on Suspension Coils (Deliverable 3)

Using R, t-tests were performed to "determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch."

Before testing, we are assuming: <br>
the null hypothesis (H0) to indicate that there is no statistical difference between the lot and the population mean, where as <br> 
the alternative hypothesis (H1) assumes there is a statistical difference between the lot and the population mean.

<b>All Lots</b> (p > 0.05)<br>
![](resources/Deliverable_3a.PNG)<br>
<b>Lot1</b> (p > 0.05)<br>
![](resources/Deliverable_3b.PNG)<br>
<b>Lot2</b> (p > 0.05)<br>
![](resources/Deliverable_3c.PNG)<br>
<b>Lot3</b> (p < 0.05)<br>
![](resources/Deliverable_3d.PNG)<br>

<b>Summary:</b><br>In order to determine if the lots are significantly different from the population mean, we can reference our p-values to draw our conclusion.
<br><br>Should the p-value be higher than 0.05 (> 0.05), it is an indication that it is not statistically significant and indicates evidence for the null hypothesis.
Here we can fail to reject the null hypothesis and reject the alternative hypothesis. As shown above, all the lots combined have a p-value greater than 0.05 (p=0.06), which means that all the lots combined have no statistical difference from the population mean. Further, both Lot1 (p=1) and Lot2 (p=0.61) have p-values greater than 0.05, which again we fail to reject the null hypothesis and claim there is no statistical difference from the population mean.
<br><br>In contrast, the summary shows for Lot3 a p-value of 0.04, which means it's less than 0.05 (p < 0.05). A p-value less than 0.05 indicates statistical significance. It's strong evidence to reject the null hypothesis and not enough information to reject the alternative hypothesis. In our test for Lot 3, we can derive that it's statistically significant and assume there is a statistical difference between the lot and the population mean.

---
## Study Design: MechaCar vs Competition

<i>Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating. </i><br>

<i><b>What metric or metrics are you going to test?</b></i><br>
The cost of a vehicle and it's comparison to the competition would be ideal to consider for a statistical study. So, for a study design
I would consider <b>cost</b> for testing the MechaCar vehicle against a population average cost of similar vehicles from other manufacturers. 
In addition, I would like to see how other competitors measure against the population and compare them to MechaCar.

<i><b>What is the null hypothesis or alternative hypothesis?</b></i><br>
(H0): There is no statistical difference between the vehicle and the population mean.<br> 
(H1): There is a statistical difference between the vehicle and the population mean.

<i><b>What statistical test would you use to test the hypothesis? And why?</b></i><br>
Resembling the lots exercise in Deliverable 2 and 3, I would consider running similiar statistical tests. First, I would run a summary statistics test to determine the average
vehicle cost. Next, I would perform t-tests of each vehicle (both MechaCar and other competitors) and determine if there is a statistical difference from the population mean.
Should the p-value of each test be greater than 0.05, I can say that the cost of the vechile has no statistical difference from the mean and assume the cost is around market-price. However, should the p-value be less than 0.05, it can be inferred that there is a statistical difference from the population. Further, it can be assumed that the cost of the vehicle is either overpriced or undervalued compared to market. Lastly, we'd be able compare the results of each t-test and determine how the MechaCar vehicle fares against the competitors. We can address whether the MechaCar is priced correctly against the market and if it's competitive against the other manufacturers.

<i><b>What data is needed to run the statistical test?</b></i><br>
In order to perform the outlined statistical tests, the data gathered would need to reflect the manufacturers (including AutosRUs'), vehicleID of all the prototypes simliar to the MechaCar, and the cost of each vehicleID. 
