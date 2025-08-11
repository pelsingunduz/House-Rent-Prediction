# House-Rent-Prediction
- EDA: distribution plots, city-wise boxplots, scatter (Size vs Rent), correlation heatmap
- Robust `Floor` parser → numeric `current_floor` and `total_floors`
- Drop high-cardinality/explanatory columns; clip `Size` outliers to 1–99% range
- **Pipeline**: median imputation + StandardScaler for numeric, One-Hot Encoding for categorical
- **Log1p** transform on target (`Rent`) to reduce right-skew; back-transform at evaluation/inference
- Models: Linear Regression, Random Forest (300 trees)
- Metrics: **R², RMSE, MAE** computed on the original currency scale
- Persist best model (`joblib`) + metadata (`JSON`)
