# Model Equations

## Simple Regression Equations

### Simple Model 1: marketing spend

Equation: `monthly_sales = 560,777.3454 + 2.1296*marketing_spend`

- R-squared: 0.167
- Coefficient for `marketing_spend`: 2.130
- P-value: <0.001
- Business meaning: a one-unit increase in marketing spend is associated with a higher monthly sales level of about 2.13, holding nothing else constant. This variable appears statistically useful.

### Simple Model 2: footfall

Equation: `monthly_sales = 446,410.5829 + 35.6780*footfall`

- R-squared: 0.736
- Coefficient for `footfall`: 35.678
- P-value: <0.001
- Business meaning: a one-unit increase in footfall is associated with a higher monthly sales level of about 35.68, holding nothing else constant. This variable appears statistically useful.


## Multiple Regression Equation

Equation: `monthly_sales = 404,245.3897 + 1.1376*marketing_spend + 33.5648*footfall - 88,560.5906*avg_discount_pct + 10,436.8770*region_west`

- `Intercept`: expected baseline monthly sales when all numerical predictors are zero and the store is in the reference category. P-value: <0.001.
- `marketing_spend`: each one-unit increase/change is associated with an increase of about 1.14 in monthly sales, assuming the other predictors stay the same. P-value: <0.001.
- `footfall`: each one-unit increase/change is associated with an increase of about 33.56 in monthly sales, assuming the other predictors stay the same. P-value: <0.001.
- `avg_discount_pct`: each one-unit increase/change is associated with a decrease of about 88,560.59 in monthly sales, assuming the other predictors stay the same. P-value: 0.026.
- `region_west`: each one-unit increase/change is associated with an increase of about 10,436.88 in monthly sales, assuming the other predictors stay the same. P-value: 0.081.


## Multiple Regression Business Interpretation

- Intercept: 404,245 is the model baseline for the reference category (`East`) when the numerical predictors are zero. Because zero footfall, zero marketing spend, and zero discount may not describe a real operating store, the intercept should mainly be treated as a mathematical starting point.
- `marketing_spend`: coefficient 1.14, p-value <0.001. Direction is positive. Business meaning: a one-unit increase in marketing spend is associated with about 1 more monthly sales, holding the other model variables constant. This is statistically useful in this model.
- `footfall`: coefficient 33.56, p-value <0.001. Direction is positive. Business meaning: a one-unit increase in footfall is associated with about 34 more monthly sales, holding the other model variables constant. This is statistically useful in this model.
- `avg_discount_pct`: coefficient -88,560.59, p-value 0.026. Direction is negative. Business meaning: a one-unit increase in avg discount pct is associated with about 88,561 less monthly sales, holding the other model variables constant. This is statistically useful in this model.
- `region_west`: coefficient 10,436.88, p-value 0.081. Direction is positive. Business meaning: stores in this category are estimated to differ from the reference category `East` by about 10,437 in monthly sales, after accounting for the numerical predictors. This is borderline and should be interpreted carefully.

Variables with weaker evidence: `region_west`. These may still matter operationally, but this model does not isolate them as strongly as the significant predictors.

## Dummy Variables

The categorical variable `region` was converted to dummy variables. The reference category is `East`, so it is intentionally excluded from the model to avoid redundancy. The included dummy variable(s) are: `region_west`, `region_north`, `region_south`. A dummy coefficient shows the estimated difference from the reference category after accounting for the other predictors.

## Final Model Selected

The selected final model is the multiple regression model. It was selected because it has the strongest explanatory power among the tested models and includes both operational drivers and at least one categorical store difference through a dummy variable.
