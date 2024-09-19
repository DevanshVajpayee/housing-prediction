# housing-prediction
A machine learning model to predict housing prices based on features like location, size, and number of rooms. Trained on historical data, it uses regression techniques to estimate future prices, assisting buyers and real estate professionals. Built with Python, scikit-learn, pandas, and Matplotlib for analysis and visualization.

1. **Data Loading and Preprocessing**:
   - The dataset is loaded, and unnecessary columns (`id`, `date`) are dropped.
   - A correlation matrix is visualized to understand relationships between variables, and the top correlated feature with price is `sqft_living` (0.702).

2. **Simple Linear Regression**:
   - The first regression uses `sqft_living` to predict house prices. 
   - The RMSE is **276,559**, and the R² value is **0.494**, suggesting a poor fit.

3. **Multiple Linear Regression**:
   - Top 10 correlated features are selected for multiple regression: `sqft_living`, `grade`, `sqft_above`, `sqft_living15`, `bathrooms`, `view`, `sqft_basement`, `bedrooms`, `lat`, and `waterfront`.
   - The RMSE improves to **226,416**, and R² is **0.661**, showing a better but still imperfect fit.

4. **Multiple Regression with All Features**:
   - Using all available features, the model shows further improvement with an RMSE of **212,539** and R² of **0.701**, demonstrating a stronger predictive capability.

**Conclusion**: More features improve prediction accuracy, but potential overfitting and feature scaling may affect results. You could try additional techniques like polynomial regression, or regularization methods to further enhance the model’s performance.
