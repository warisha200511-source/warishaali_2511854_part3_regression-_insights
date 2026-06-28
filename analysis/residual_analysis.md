# Residual Analysis

Predicted sales were calculated using the selected multiple regression model. Residuals equal actual monthly sales minus predicted monthly sales. Positive residuals mean the store sold more than the model expected. Negative residuals mean the store sold less than expected.

## Largest Positive Residuals

| Record | store_id | Actual sales | Predicted sales | Residual |
| --- | --- | --- | --- | --- |
| 1 | STR-1028 | 713,611 | 595,587 | 118,024 |
| 2 | STR-1026 | 625,514 | 514,891 | 110,623 |
| 3 | STR-1032 | 914,544 | 812,299 | 102,245 |
| 4 | STR-1064 | 799,047 | 700,141 | 98,906 |
| 5 | STR-1075 | 763,162 | 666,892 | 96,271 |

These records may represent stores outperforming the model because of factors not captured in the dataset, such as local events, stronger execution, product mix, competitive conditions, or unusually effective promotions.

## Largest Negative Residuals

| Record | store_id | Actual sales | Predicted sales | Residual |
| --- | --- | --- | --- | --- |
| 1 | STR-1012 | 595,468 | 740,017 | -144,550 |
| 2 | STR-1017 | 685,379 | 819,073 | -133,694 |
| 3 | STR-1009 | 641,865 | 766,187 | -124,322 |
| 4 | STR-1023 | 627,172 | 745,356 | -118,184 |
| 5 | STR-1001 | 658,920 | 772,898 | -113,977 |

These records may represent stores underperforming the model expectation. The model may be over-predicting these stores because it does not capture local constraints, stock quality, staffing, competition, weather, or other operational issues.


## Under-Prediction and Over-Prediction by region

| Category | Records | Average residual | Pattern |
| --- | --- | --- | --- |
| East | 104 | -9,177 | Over-predicting on average |
| West | 92 | -0 | Over-predicting on average |
| North | 64 | 4,118 | Under-predicting on average |
| South | 60 | 11,515 | Under-predicting on average |

On average, positive residual categories are being under-predicted by the model, meaning actual sales are higher than predicted. Negative residual categories are being over-predicted. Because the final model includes only the West dummy and uses East as the reference category, remaining regional differences for North and South may still be partly sitting in the residuals.

## Pattern Check

The residuals should be reviewed by region and by the strongest numerical predictors. Large residuals do not automatically mean data errors; they highlight stores where leadership should ask what the model is missing.
