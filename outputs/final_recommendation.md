# Final Recommendation

The factors most strongly associated with monthly sales in the selected model are `footfall`, `marketing_spend`, `avg_discount_pct`. The selected multiple regression model has an R-squared of 0.787, which means it explains about 78.7% of the observed variation in monthly sales.

Leadership should focus first on variables with meaningful coefficients and useful p-values, especially footfall, marketing spend, avg discount pct. These are the predictors most likely to help prioritize actions such as marketing allocation, traffic generation, inventory availability, discount planning, or store-format decisions.

Variables that should not be over-interpreted include `region_west`, because their p-values are weaker or their business meaning may overlap with other predictors. A weak p-value does not prove a variable is useless; it means this dataset does not provide strong separate evidence for that variable after accounting for the model.

The recommended action is to use the multiple regression model as a decision-support tool, then investigate the largest positive and negative residual stores. Stores beating the model may reveal repeatable practices, while stores falling short may need operational review.

Key limitations: the model only includes variables in the dataset, it may omit local market conditions, seasonality, competition, staffing, pricing mix, and promotion timing, and it shows association rather than automatic causation. Regression can show that sales move with a factor, but it cannot by itself prove that changing that factor caused the sales change; experiments, time-based evidence, or stronger controls would be needed for causal claims.
