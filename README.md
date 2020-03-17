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







