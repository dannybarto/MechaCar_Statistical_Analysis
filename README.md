# Mechacar_Statistical_Analysis

### Background
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, you’ll help Jeremy and the data analytics team do the following:

* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Deliverables:
The assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:

1. ***Deliverable 1:*** Linear Regression to Predict MPG
2. ***Deliverable 2:*** Summary Statistics on Suspension Coils
3. ***Deliverable 3:*** T-Test on Suspension Coils
4. ***Deliverable 4:*** Design a Study Comparing the MechaCar to the Competition


## Deliverables:
This new assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:

* Data Sources: MechaCar_mpg.csv and Suspension_Coil.csv
* Data Tools:  tidyverse/dplyr/ggplot2/MechaCarChallenge.RScript
* Software: RStudio/R

# Deliverable 1:  
## Linear Regression to Predict MPG
### Deliverable 1 Overview:

The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using your knowledge of R, you’ll design a linear model that predicts the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.csv file. All of this shall be included in a short, written interpratation of the multiple linear regression results.

### Deliverable 1 Requirements:
- The MechaCar_mpg.csv file is imported and read into a dataframe
- An RScript is written for a linear regression model to be performed on all six variables
- An RScript is written to create the statistical summary of the linear regression model with the intended p-values
- There is a summary that addresses all three questions


#### Deliverable 1 Results:
**Resulting Model:** 

### mpg =  (6.267)**vehicle_length** + (0.0012)**vehicle_weight** + (0.0688)**spoiler_angle** + (3.546)**ground_clearance** + (-3.411)**AWD** + (-104.0)
				

**Statistical Summary:** 
![d1](https://github.com/dannybarto/MechaCar_Statistical_Analysis/blob/30182147017652bdd767c21830f52171b2d9821d/Resources/Images/Linear_Regression_1.png)

## Observations:

1. Vehicle length, and vehicle ground clearance*are statistically likely to provide non-random amounts of variance to the model. In other words, the vehicle length and vehicle ground clearance appear to  have a significant impact on miles per gallon on the MechaCar prototype. On the other hand,
the vehicle weight, spoiler angle and all wheel drive (AWD) variables have p-Values that indicate a random amount of variance within the dataset.  

2. The p-Value for this model (p-Value: 5.35e-11) is less than the assumed significance level of 0.05% by a fair amount. This evidence lends support to rejecting the null hypothesis. We can safely assume  that the slope of this linear model is not 0.


3.  The linear model has an r-squared value of 0.7149, which indicates that roughly 71.5% of all mpg predictions can be determined using the modell. The multiple regression model does not appear to accuratelty predict the mpg of MechaCar prototypes. 

The predictability does indeed decrease when removing vehicle weight/spoiler angle/AWD. The r-squared value decreases from 0.7149 as indicated above to 0.674. 

![d1](https://github.com/dannybarto/MechaCar_Statistical_Analysis/blob/30182147017652bdd767c21830f52171b2d9821d/Resources/Images/Linear_Regression_Sum.png)


# Deliverable 2:  
## Create Visulizations for the Trip Analysis
### Deliverable 2 Overview:

The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. A summaryt statistics table will be created by utilizing R and it will show the following:

- The suspension coil’s PSI continuous variable across all manufacturing lots
- The following PSI metrics for each lot: mean, median, variance, and standard deviation.

#### Brief Detail and Interpretation of the Suspension Coil Summary Statistics
1. Download the Suspension_Coil.csv file, and place it in the active directory for your R session.
2. In your MechaCarChallenge.RScript, import and read in the Suspension_Coil.csv file as a table.
3. Write an RScript that creates a total_summary dataframe using the summarize() function to get the mean, median, variance, and standard deviation of the suspension coil’s PSI column.

View of the Total_Summary Dataframe:

![d1](https://github.com/dannybarto/MechaCar_Statistical_Analysis/blob/30182147017652bdd767c21830f52171b2d9821d/Resources/Images/Suspension_Coils_1.png)

4. Write an RScript that creates a lot_summary dataframe using the group_by() and the summarize() functions to group each manufacturing lot by the mean, median, variance, and standard deviation of the suspension coil’s PSI column.

View of the Lot_Summary Dataframe

![d1](https://github.com/dannybarto/MechaCar_Statistical_Analysis/blob/30182147017652bdd767c21830f52171b2d9821d/Resources/Images/Suspension_Coils_2.png)

5. Save your MechaCarChallenge.RScript file to your GitHub repository.

### Deliverable 2 Requirements:

- The Suspension_Coil.csv file is imported and read into a dataframe
- An RScript is written to create a total summary dataframe that has the mean, median, variance, and standard deviation of the PSI for all manufacturing lots
- An RScript is written to create a lot summary dataframe that has the mean, median, variance, and standard deviation for each manufacturing lot
- There is a summary that addresses the design specification requirement for all the manufacturing lots and each lot individually

The results of testing the weight capacities of supension coils can be derived from the the supension coil dataset.

1. A view of all manufacturing lots:

![d2](https://github.com/dannybarto/MechaCar_Statistical_Analysis/blob/30182147017652bdd767c21830f52171b2d9821d/Resources/Images/Suspension_Coils_1.png)

2. More granular view of each of the lots individually

![d2](https://github.com/dannybarto/MechaCar_Statistical_Analysis/blob/30182147017652bdd767c21830f52171b2d9821d/Resources/Images/Suspension_Coils_2.png)

The design specifications for the MechaCar suspension coils call for a variance that does not exceed 100 PSI.

A review of the total population fo the production lots shows a variance of 62.3 PSI. This falls within the within the 100 PSI requirement.

T-test() to determine if PSI across all mfg lots is statistically different from population mean of 1500 PSI

![d3](https://github.com/dannybarto/MechaCar_Statistical_Analysis/blob/30182147017652bdd767c21830f52171b2d9821d/Resources/Images/R_Plot.png)


# Deliverable 3:  
### Deliverable 3 Overview:

Using your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

#### Technical Analysis and Requirements
1. In your MechaCarChallenge.RScript, write an RScript using the t.test() function to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.
2. Next, write three more RScripts in your MechaCarChallenge.RScript using the t.test() function and its subset() argument to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.

- An RScript is written for t-test that compares all manufacturing lots against mean PSI of the population
- An RScript is written for three t-tests that compare each manufacturing lot against mean PSI of the population
- There is a summary of the t-test results across all manufacturing lots and for each lot

 A t-test on the suspension coil data is necessary  to determine if there is a statistical difference between the mean of the current sample dataset and a hypothesized, potential dataset. 

The following is a summary of the t-test results across all manufacturing lots assuming a population mean of 1500:
![d3](https://github.com/dannybarto/MechaCar_Statistical_Analysis/blob/30182147017652bdd767c21830f52171b2d9821d/Resources/Images/T-Test_1.png)
![d4](https://github.com/dannybarto/MechaCar_Statistical_Analysis/blob/30182147017652bdd767c21830f52171b2d9821d/Resources/Images/T-Test_2.png)

This demonstrates a true sample mean of 1498.78. This corroborates our summary statistics.  At a p-Value of 0.06 there is not sufficient evidence to support rejection of the null hypothesis The mean of all the lots is within the 1500 range.

1. Lot has sample mean of 1500. With this we cannot reject the null hypothesis that there isn't a statistical difference between the sample mean nand the potential population mean.
2. Lot 2 is not far off from the 1500 we want to see with sample mean of 1500.02, as well as a p-Value of 0.61. As with Lot 1, the null hypothesis cannot be rejected.
3. Lot 3, is a little different as noted above. The sample mean here is 1496.14 with a p-Value of 0.04. This is actually lower than the  which is lower than the common significance level of 0.05. Based on this we could make the argument to reject the null hypothesis.

# Deliverable 4:  
## Study Design: MechaCar vs Competition
### Deliverable 47 Requirements:

Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

The statistical study design has the following:
- A metric to be tested is mentioned
- A null hypothesis or an alternative hypothesis is described
- A statistical test is described to test the hypothesis


This study would involve collecting data on MechaCar and its comparable models across several different manufacturers over the last 3 years.

* What are the competitions" comparable models, 
* Which cars will MechaCar be competing with head-to-head? which cars will be included in the study?
* Which factors will look at the study to determine the relevant to selling price?
 

#### What Metric or Metrics Are You Going to Test?
Gather comparable model data for the following across relevant manufacturers for the last 2 to 5 years

* Price (What the consumer pays)
* Fuel Efficency (City/Highway)
* Horse Power
* Maintenance
* Safety Rating

#### Hypothesis: Null and Alternative
 * Null Hypothesis: The MechaCar is reasonably priced based on analysis of the gathered data
 * Alternative Hypothesis: MechaCar is not priced reasonably based on analysis of the gathered data
 
#### Data Needed to Run the Statistical Test
Multiple linear regression should be used to determine which factors are most likely to correlate to the final selling price the vehicle
