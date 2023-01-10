# BigMart_Sales
It's sales data project on different items at multiple outlets of a major retail chain. It's a multi-level data project.

# Multi-level Dataset
Level 1: Items (Item_ID, Item_MRP, Item_Desc), and 
Level 2: Outlets (Outlet_ID, Outlet_Type).
Hence, I have used multi-level analysis for this project. 

# Regression Models:
Since my data is multi-level, so I have used OLS model to compare against fixed and random effects models, but my interpretation will be based on fixed or random effects models only. As an alternative, I also ran multiple FE and RE models with interaction effects!

 Model Performance:

=====================================================================================================
                                              Dependent variable: log(Item_Sales)              
                               ----------------------------------------------------------------------
                                         ols                         fe                    re
-----------------------------------------------------------------------------------------------------
Item_Visibility                       0.023 (0.114)               0.019 (0.114)         0.021 (0.114)  
Item_TypeBreads                       0.041 (0.039)               0.042 (0.038)         0.041 (0.038)  
Item_TypeBreakfast                    -0.064 (0.053)              -0.065 (0.053)        -0.065 (0.053) 
Item_TypeCanned                       0.023 (0.029)               0.023 (0.029)         0.023 (0.029)  
Item_TypeDairy                        -0.030 (0.028)              -0.031 (0.028)        -0.030 (0.028) 
Item_TypeFrozen Foods                 -0.021 (0.027)              -0.022 (0.027)        -0.021 (0.027) 
Item_TypeFruits and Vegetables        -0.001 (0.025)              -0.001 (0.025)        -0.001 (0.025) 
Item_TypeHard Drinks                  -0.003 (0.041)              -0.002 (0.041)        -0.003 (0.041) 
Item_TypeHealth and Hygiene           0.015 (0.031)               0.015 (0.031)         0.015 (0.030)  
Item_TypeHousehold                    -0.016 (0.027)              -0.016 (0.027)        -0.016 (0.027) 
Item_TypeMeat                         0.022 (0.032)               0.021 (0.032)         0.021 (0.032)  
Item_TypeOthers                       -0.005 (0.045)              -0.004 (0.045)        -0.005 (0.045) 
Item_TypeSeafood                      0.028 (0.068)               0.028 (0.068)         0.028 (0.068)  
Item_TypeSnack Foods                  -0.006 (0.025)              -0.006 (0.025)        -0.006 (0.025) 
Item_TypeSoft Drinks                  -0.003 (0.032)              -0.003 (0.032)        -0.003 (0.032) 
Item_TypeStarchy Foods                -0.001 (0.047)              -0.002 (0.047)        -0.001 (0.047) 
log(Item_MRP)                        1.023*** (0.011)            1.023*** (0.011)      1.023*** (0.011)
Outlet_TypeSupermarket Type1         1.939*** (0.020)            1.690*** (0.158)      1.938*** (0.025)
Outlet_TypeSupermarket Type2         1.751*** (0.038)            1.568*** (0.135)      1.756*** (0.049)
Outlet_TypeSupermarket Type3         2.511*** (0.026)            2.755*** (0.159)      2.511*** (0.035)
City_TypeTier 2                       -0.017 (0.020)            -0.137*** (0.052)       -0.016 (0.027) 
City_TypeTier 3                       -0.027 (0.018)             -0.284* (0.159)        -0.030 (0.024) 
Outlet_Age                            -0.002 (0.001)             -0.020* (0.012)        -0.002 (0.002) 
Outlet_IDOUT013                                                   0.464 (0.290)                        
Outlet_IDOUT017                                                   -0.024 (0.065)                       
Outlet_IDOUT018                                                                                        
Outlet_IDOUT019                                                                                        
Outlet_IDOUT027                                                                                        
Outlet_IDOUT035                                                   0.055 (0.034)                        
Outlet_IDOUT045                                                                                        
Outlet_IDOUT046                                                                                        
Outlet_IDOUT049                                                                                        
Constant                             0.673*** (0.065)            1.187*** (0.341)      0.671*** (0.071)
-------------------------------------------------------------------------------------------------------
Observations                              8,523                       8,523                 8,523      
R2                                        0.742                       0.742                            
Adjusted R2                               0.741                       0.741                            
Log Likelihood                                                                            -6,471.138   
Akaike Inf. Crit.                                                                         12,994.280   
Bayesian Inf. Crit.                                                                       13,177.590   
Residual Std. Error                 0.518 (df = 8499)           0.517 (df = 8496)                      
F Statistic                    1,059.981*** (df = 23; 8499) 940.052*** (df = 26; 8496)                 
=======================================================================================================
### AIC and BIC shows that the RE model has the best fit.

## Result: I recommend opening Type 1 supermarket in a Tier 1 city if possible.
If Tier 1 city is not possible, Tier 3 city is the next best choice.

