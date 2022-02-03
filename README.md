# Overview
In this analysis, we analyze the MechaCar, a protoype for AutosRUs. Using the programming language R, we will begin to gather metrics that will show evidence of production issues that have been preventing the company's ability to progress. 



## Linear Regression to Predict MPG
The [MechaCar_mpg.csv](https://github.com/nvuono625/MechaCar_Statistical_Analysis/blob/main/R_Analysis/MechaCar_mpg.csv) dataset includes 50 prototype MechaCar's Miles Per Gallon (MPG) test results. The independent variables are the metrics for each vehicle, which include vehicle length, vehicle weight, spoiler angle, ground clearance, and all wheel drive (AWD). The dependent variable is MPG. 

![/Resources/Linear_Regression_to_Predict_MPG.png](/Resources/Linear_Regression_to_Predict_MPG.png)

### Results
- Both vehicle length and ground clearance provide a non-random amount of variance to the MPG values in the dataset.
- The slope of the linear model is not considered to be zero. The results above show that some of the independent variables are statistically significant.
- Whether or not the linear model effectively predicts the MPG of the MechaCar prototypes is up to interpretation. The R-squared value is 0.7149, so it is a 71% effectiveness.



## Summary Statistics on Suspension Coils
The [Suspension.csv](https://github.com/nvuono625/MechaCar_Statistical_Analysis/blob/main/R_Analysis/Suspension_Coil.csv) data includes weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. The design specifications for the suspensions coils state that the variance of the suspension coils must not exceed 100 pounts per square inch (PSI).

### PSI Metrics for Manufacturing Lots (Average)
An average of all three lots were calculated and developed into a table to show the summary of PSI metrics:

![/Resources/Total_Summary_Statistics_on_Suspension_Coils.png](/Resources/Total_Summary_Statistics_on_Suspension_Coils.png)

### PSI Metrics for Manufacturing Lots (Individual)
In this table, it shows the PSI metrics of each individual lot:

![/Resources/Lot_Summary_Statistics_on_Suspension_Coils.png](/Resources/Lot_Summary_Statistics_on_Suspension_Coils.png)

### Results
- Looking at the average of all three lots, the variance appears to meet design specifics, however, when we look at each lot individually only Lot 1 and Lot 2 meet the design specification and should be used. Lots 3 has a variance of 170.2861224 and therefore does not meet the design specification and should not be used.



## T-Tests on Suspension Coils
Next, T-Tests were performed on all manufacturing lots and each manufacturing lot individually. To tell whether or not the results of each lot are statistically significant, confidence intervals or p-values are used. The confidence interval is 95%, therefore the significance level is 0.05. 

![/Resources/T-Tests_on_Suspension_Coils.png](/Resources/T-Tests_on_Suspension_Coils.png)

### Results
- When looking at the metrics for all lots, a p-value of 0.06028 was recorded. Now, because the p-value is higher than 0.05, it indicates evidence to maintain the null hypothesis.
- When looking at each lot individually, Lot 1 has a p-value of 1 and Lot 2 has a p-value of 0.06072 which also indicates evidence to maintain the null hypothesis. However, Lot 3 has a p-value of 0.04168 which is below 0.05, giving us evidence to reject the null hypothesis.



## Study Design: MechaCar vs Competition

To study the MechaCar vs Competition, further analysis will need to be conducted to gather metrics from other car manufacturaters and compare it to the metrics of the MechaCar.

### Metrics
- Vehicle Type: Car, Truck, Van, Minivan, SUV, Wagon, diesal engine, hybrid, coupe, convertible, 2-Wheel Drive, 4-Wheel drive.
- Fuel Efficiency: City MPG, Highway MPG.

### Hypothesis
- The null hypothesis would be that the fuel efficiency across vehicle type is performs statistically identical between the MechaCar and other manufacturers.
- An alternative hypothesis would be needed if the fuel efficiency across vehicle type does not compare similarly between the MechaCar and other manufacturers.

### Statistical Tests
- A boxplot will show variability of the MechaCar and other manufacturers.
- T-Test can be used to distinguish statistical significant differences.

### Data Needed
- To determine fuel efficiency, calculations for city MPG and highway MPG are needed. And to determine vehicle type, the sample size will need to be similar to the sample size of the MechaCar. 
