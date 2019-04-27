# Geographically Weighted Cox Regression

This repository contains code for the manuscript *Geographically Weighted Cox
Regression and Its Application to Prostate Cancer Survival Data in Louisiana* by
Yishu Xue, Elizabeth D. Schifano and Guanyu Hu.

<a href="https://zenodo.org/badge/latestdoi/183830436"><img src="https://zenodo.org/badge/183830436.svg" alt="DOI"></a>

## real_data

`louiscounty.RData` contains the geographical information about counties in
Louisiana. 

`graphDist.RData` contains the matrix of graph distance between Louisiana counties,
calculated using the `netdistance` function in **netmeta** package.


`circDist.RData` contains the matrix of great circle distance between centroids of
Louisiana counties, calculated using the `distCosine` function in **geosphere** package.


## simulation

`genData.R` contains the function to simulate survival data with exponential baseline
hazard function, user-specified parameter vector, and tunable censoring distribution.

`nulldata.R`, `alterdata1.R`, and `alterdata2.R` contain the code
to generate the dataset for the null setting where there is no spatial
variation in the coefficients, and the two alternative setting where there
exists spatial variation. 

`simunull.R` contains the code to fit geographically weighted Cox models
and local Cox models for the null dataset with no spatially varying
coefficients using the great circle distance.

`simalter_1.R` contains the code to fit geographically weighted Cox models and local
Cox models for `alterdata1.RData` (generated by `alterdata1.R`) using the graph distance.

`process.R` is a helper function to calculate the four performance measures for simulation
replicates.


