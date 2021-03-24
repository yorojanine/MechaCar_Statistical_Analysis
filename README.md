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
(2) The following PSI metrics for each lot: mean, median, variance, and standard deviation.<br>
![](resources/Deliverable_2a.PNG) ![](resources/Deliverable_2b.PNG) <br>
<i>The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?</i><br>



---

## T-Tests on Suspension Coils

<b>All Lots</b><br>
![](resources/Deliverable_3a.PNG)<br>
<b>Lot1</b><br>
![](resources/Deliverable_3b.PNG)<br>
<b>Lot2</b><br>
![](resources/Deliverable_3c.PNG)<br>
<b>Lot3</b><br>
![](resources/Deliverable_3d.PNG)<br>

<b>Summary:</b>

---
## Study Design: MechaCar vs Competition

<i>Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating. </i><br>


<i><b>What metric or metrics are you going to test?</b></i><br>

<i><b>What is the null hypothesis or alternative hypothesis?</b></i><br>

<i><b>What statistical test would you use to test the hypothesis? And why?</b></i><br>

<i><b>What data is needed to run the statistical test?</b></i><br>
