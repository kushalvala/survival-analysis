# Survival Analysis

Generally, Survival Analysis is collection of procedure for analysis for which outcome variable is : *Time until an event  occurs*    
This set of statistical methods are different from classification algorithms, where we are interested to find patterns among the data, given the labels
Here the focus is whether the subject had an outcome of interest but also how *long* it took them to get the *outcome*

Survival Analysis can be used to explore relations between factors of interest and time to any binary event.  

## Data:

1. Heart Disease Dataset:  

The dataset consist's of 1000 patients which were observed in the hospital post having a cardiac arrest.   
There are 31 features which were monitored for a patient. 

### Kaplan Meier Plot (KM Plot)

Survival Time: Follow Up Time i.e Time Since Admission in Hospital (in days) 

Event: Death of Patient 

KM Plot for all patients:

![KM Plot](https://github.com/kushalvala/survival-analysis/blob/master/figures/KMPlot.png)

Median Survival Time : 719 days

Confidence Interval of 95% : [685, 793] days

KM Plot for Gender:

![Gender](https://github.com/kushalvala/survival-analysis/blob/master/figures/KMPlot-Gender.png)

To check if there is similarity between two survival probability functions, we use a Log Rank Test 

Results of Log Rank Test:

p-value : 0.7745 ( > 0.05 )

p-value is much greater than the set alpha value. 
We cannot discard the Null Hypothesis i.e both the survival graphs are similar.


### Cox Proportional Hazard Model (CoxPH Model)

This method is also called Survival Regression, which mathematically models the survival time along with other confounding variables, and outputs the hazard ratio's.
The advantage this method holds over the KM Plot is that we can regress multiple variable as compared to building a univariate analysis.

Here we built a model with a our earlier problem statement, where we are adding two confounding variables:
  1. Ethnic Group
  2. Gender

We are interested to see if there is a relation between this variables and the event ( ~ death ) 

Summary Statistic of CoxPH Model is very similar to that of a typical Regression plot. Only difference is it outputs a Hazard Ratio, which gives us the measure of how critical that particular element is for a given event.

Below is the plot:

![Summary](https://github.com/kushalvala/survival-analysis/blob/master/figures/CoxPH%20Analysis.png)

We can clearly see that hazard ratio for ethnic group-3 is 0.33 which is lower than baseline, and we can conclude that the patients belonging to that group has lower risk of the event being occured in their case.









