Group number: 12 
------------------

Group Members : Shuang Yang (2614596)  Ruofan Wang(2627659) Jiayi  Wang(2648246) Yilei  Ma(2612840)
------------------

## Research question: What factors influence the number of days an animal spends in a shelter before deciding its final outcome？

## The installation package:
library(ggplot2)
library(qcc)
library(arm)
library(jtools)
library(ggstatsplot)
library(pscl)
library(lmtest)
library(ggpubr)
library(broom)
library(ggstance)
library(MASS)



## Background

The Dallas Animal Shelter recorded the number of days each animal spent at the shelter in 2016 and 2017, and recorded additional information about the animals. It can be found that the factors in the data set have a certain impact on the number of days to be taken in. Our team wanted to calculate the correlation between these factors and the final number of days to be taken in, so the team chose THE GLM Poisson regression model to analyze the data. Poisson distribution in the generalized linear model can directly express the strength of the correlation between independent variables and dependent variables composed of discrete data. Meanwhile, additional explanations are needed for missing values and outliers in the data set, as well as for the comparison of the influence degree of the last several factors on the final days of detention.

## Aims of the analysis

By analysing data from animal shelters, the main factors influencing the number of days animals spend in shelters are identified and given to animal shelter managers for information.


## The main method

The glm model was used for this analysis, and the Poisson distribution was chosen for the family of distributions. After model testing, we concluded that the Poisson-like model was more suitable for this modelling. 


## Conclusion

Compared to the Poisson model, the modified Poisson-like model has a larger standard error. After reading the relevant literature, we know that we should use the p-value of the Poisson-like model as a measure.


## Future jobs

In future work, we will consider corrections for y-value dispersion - too many zero values - such as the zero-inflated model.
