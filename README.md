# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG
Summary: After reading in the `MechaCar_mpg.csv` file, the lm() function is used to pass in all six variables (columns from the dataset) to determine their coefficients. 
The function is used for building linear models, in which it takes in two main arguements 1. Formula 2. Data. Here in the function, the "Formula" is taking in the six variables,
whereas the "Data" is the dataframe created when we brought in the csv file. 

### Multiple Linear Regression Model 
![](resources/Deliverable_1a.PNG)

### Multiple Linear Regression Model Summary
In order to run the summary of the regression model to ensure it's statistically signficant, there are two options to run it (both using the summary() function).
First, you can just pass the lm() formula we wrote as is through the summary () function -or- assign the lm() formula a variable and pass that variable through the summary() funtion. Either way, the results are the same.
![](resources/Deliverable_1b.PNG)
![](resources/Deliverable_1c.PNG)

<i>Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?</i><br>
answer.

<i>Is the slope of the linear model considered to be zero? Why or why not?</i><br>
The slope is not considered to be zero as the intercept determines 

<i>Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?</i>

---

## Summary Statistics on Suspension Coils

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
