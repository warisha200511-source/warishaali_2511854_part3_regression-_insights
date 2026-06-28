# Model Comparison

| Model name | Dependent variable | Independent variables | R-squared | Adjusted R-squared | Significant variables | Business usefulness | Limitations |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Simple Model 1: marketing spend | monthly_sales | marketing_spend | 0.167 | 0.165 | marketing_spend | Useful as a one-variable diagnostic, but incomplete for planning. | Association only; excludes factors not in the dataset and may reflect correlated store conditions. |
| Simple Model 2: footfall | monthly_sales | footfall | 0.736 | 0.735 | footfall | Useful as a one-variable diagnostic, but incomplete for planning. | Association only; excludes factors not in the dataset and may reflect correlated store conditions. |
| Multiple Model: operating drivers plus dummy variable | monthly_sales | marketing_spend, footfall, avg_discount_pct, region_west | 0.787 | 0.785 | marketing_spend, footfall, avg_discount_pct | Best overall explanatory model among those tested because it combines operating drivers and category differences. | Association only; excludes factors not in the dataset and may reflect correlated store conditions. |

## Overall Interpretation

The simple models show how each single business driver relates to monthly sales on its own. The multiple model is more useful for leadership because it compares several drivers at the same time and includes a dummy variable for region. R-squared improves from the simple models to the multiple model, which means the combined model explains more of the sales variation in this dataset.
