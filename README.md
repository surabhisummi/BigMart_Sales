# BigMart_Sales
It's sales data project on different items at multiple outlets of a major retail chain. It's a multi-level data project.

## Multi-level Dataset
Level 1: Items (Item_ID, Item_MRP, Item_Desc), and 
Level 2: Outlets (Outlet_ID, Outlet_Type).
Hence, I have used multi-level analysis for this project. 

## Regression Models:
Since my data is multi-level, so I have used OLS model to compare against fixed and random effects models, but my interpretation will be based on fixed or random effects models only. As an alternative, I also ran multiple FE and RE models with interaction effects!

## Model Performance:

                                        Dependent variable: log(Item_Sales)              
                               ----------------------------------------------------------------------
                                     ols                         fe                    re
-----------------------------------------------------------------------------------------------------
Observations                      8,523                       8,523                 8,523      
R2                                0.742                       0.742                            
Adjusted R2                       0.741                       0.741                            
Log Likelihood                                                                      -6,471.138   
Akaike Inf. Crit.                                                                    12,994.280   
Bayesian Inf. Crit.                                                                  13,177.590   
Residual Std. Error              0.518 (df = 8499)           0.517 (df = 8496)                      
F Statistic                1,059.981*** (df = 23; 8499) 940.052*** (df = 26; 8496)                 
=======================================================================================================
### AIC and BIC shows that the RE model has the best fit.

## Result: I recommend opening Type 1 supermarket in a Tier 1 city if possible.
If Tier 1 city is not possible, Tier 3 city is the next best choice.

