---
title: "PS 8 Franciscians"
author: "Team Francis"
date: "3/12/2018"
output: html_document
---







## Q1

When run with S=200, the bootstrap variance is 0.029532, which is slightly larger than the exact variance  of 0.0276024. Both are larger than the asymptotic variance of 0.0235974. 

## Q2

The 95% quantile of the Wald test (4.4519988) is much lower than that of the asymptotic distribution (7.8147279).

## Q3

Average rejection rate of the Wald tests are given by 0.01.

## Q4

We calculate a Wald stat using the ratio estimate from each sample (the ratio variable) and use the bootstrap variance estimate (boot_sd_v). Using this test the rejection rate is 0.01.

## Q5

We run the second bootstrap test in which we use the Wald statistic using asymptotic variance estimator (please see Q1). Using this test the rejection rate is 0.04. We then use critical values calculated in the bootstrap procedure, both critical values calculated (one centered around beta1/beta2, the other betahat1/betahat2). Using this test the rejection rate is 0.05.

## Q6
Because the critical values found using the Wald statistic centered around the estimated value is smaller than the one centered around the true value (for each sample on which we run bootstrap), we expect that the former would have a higher rejection rate than the latter.

## Q7
The result would likely change, because the Delta method is sensitive to the way in which we define the restrictions. 


## Cross Validation Section



#1
The dimension of crossval_df is 100x3. Each cell contains a 99x3 or 1x3 list of data: each row is a resample of all three variables of data_df where 99 of the observations are in the column train and the last observation is in the column 1. The last column is an ID variable for the resample. 
Using the data in the train column, both regressions are run on each of the resamples. The data are reshaped so the regressions are contained in the "reg" column and the "model" column is a label for reg1 or reg2. Then the in-sample MSE is calculated of each of these regressions (mse_in). The "resids_out = map2_dbl(...)" line generates the residual from the prediction of the out of sample observation using the regression with rest of the data. The .x and .y refer to the first two arguments of map2_dbl: reg (the regresson with the training data) and test (the out of sample observation). Then the out of sample MSE is calculated from this residual. Finally the data are reshaped so that both MSEs are in one column (value) and the mse column labels whether the value is mse_in vs. mse_out. 


#2 
The in-sample MSE is higher for for the regression with just x1, which makes sense because it has one less explanatory variable. However, the out-sample MSE is similar for both regressions (only slightly higher for the regression with just x1) -- this is because in fact the d.g.p. only contains x1 and not x2, so adding x2 is overfitting the data. For both models, the out-sample MSE is higher than the in-sample MSE because the data are overfitted. 

|model |mse     |  mean|
|:-----|:-------|-----:|
|reg1  |mse_in  | 1.198|
|reg1  |mse_out | 1.250|
|reg2  |mse_in  | 1.164|
|reg2  |mse_out | 1.241|

#3 
The Hansen formula out-sample MSE estimates are almost identical to our simulation estimates. 

The formula estimate is 1.2498829 for regression 1 and 1.2411171 for regression 2. 
