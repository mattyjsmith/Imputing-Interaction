# Imputing Interactions
R code to compare multiple imputation approaches for a logistic regression model where the interaction includes a partially observed binary variable. 

The multiple imputation approaches are compared within six different scenarios: the first is the reference scenario and each scenario thereafter is slightly altered, such that:

1. Base-Case: MAR, binary Z, 30% p(Z), 20% missingness in X, OR=1.3
2. Low OR: MAR, binary Z, 30% p(Z), 20% missingness in X, OR=1.1
3. High OR: MAR, binary Z, 30% p(Z), 20% missingness in X, OR=1.7
4. MCAR: MCAR, binary Z, 30% p(Z), 20% missingness in X, OR=1.3
5. Continuous Z: MAR, continuous Z, NA p(Z), 20% missingness in X, OR=1.3
6. Low Z prev: MAR, binary Z, 1% p(Z), 20% missingness in X, OR=1.3

where Z is the fully observed variable, X is the partially observed variable, MAR is assuming missing at random, MCAR is assuming missing completely at random, p(Z) is the prevalence of Z, and OR is the odds ratio for the interaction.  

During the analysis, 1000 simulations were used for a data set of 100,000 observations and 10 iterations and 10 imputations were used for each multiple imputation approach.
