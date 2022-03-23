--Group number: 12 --
##Group Members : Shuang Yang (2614596)  Ruofan Wang(2627659) Jiayi  Wang(2648246) Yilei  Ma(2612840)


######### Research question: What factors influence the number of days an animal spends in a shelter before deciding its final outcome？
######### The installation package:

---------------------------------
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
---------------------------------




#########.Background

The Dallas Animal Shelter recorded the number of days each animal spent at the shelter in 2016 and 2017, and recorded additional information about the animals. It can be found that the factors in the data set have a certain impact on the number of days to be taken in. Our team wanted to calculate the correlation between these factors and the final number of days to be taken in, so the team chose THE GLM Poisson regression model to analyze the data. Poisson distribution in the generalized linear model can directly express the strength of the correlation between independent variables and dependent variables composed of discrete data. Meanwhile, additional explanations are needed for missing values and outliers in the data set, as well as for the comparison of the influence degree of the last several factors on the final days of detention.



#########.The main method

###Analyze the data
Analyze box graphs of all independent variables; Analyze the distribution of the dependent variable Y.
Evaluation: The data is not the curve form of normal distribution, and the dependent variable Y conforms to poisson distribution; Excessive dispersion appears in the model; A lot of zeros appear in the data set.

###Model selection
GLM Poisson regression model was determined to be the appropriate model because the research problem required to understand the correlation between variables and the dependent variable data conforms to poisson distribution

###Establish the GLM Poisson regression model
Include variables and build models
Model results

###Model testing
Due to excessive data with value of 0 in the data set, FIT3 model (Poisson-like distribution model) was established and parameter results of the two models were compared (parameter estimates were consistent, but standard errors were different).

###Model coefficient analysis
Conclusion: The change of Type results in fewer days in the shelter. All are significant except outcome (died), which is insignificant.

#########.Conclusion

GLM Poisson distribution model has excessive ionization phenomenon, and the standard error of Poisson like distribution model is large.

#########.Future jobs

Poisson distribution model and Poisson-like distribution model both have errors to a certain extent. Since there are too many zeros in the data set, zero-expansion Poisson regression model will be considered later
f(y_i,"λ" _i,ω_i )={█(ω_i+(1-ω_i ) e^(〖-λ〗_i ),y_i=0@((1-ω_i)e^(〖-λ〗_i ) λ_(i^(y^i ) ))/(y_i !),y_i=1,2,…,n)┤
