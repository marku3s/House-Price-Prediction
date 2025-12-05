🏠 House Price Prediction: Advanced Regression Techniques
1. Project Objective

The goal of this project is to predict residential home prices in Ames, Iowa. This is a Regression task where the target variable is SalePrice. The project demonstrates specific skills in outlier detection, feature engineering (One-Hot Encoding), and comparing linear vs. tree-based machine learning models.
2. Data Cleaning & Processing
Outlier Detection

    Visualized GrLivArea vs SalePrice.

    Identified and removed two "partial sale" outliers (Houses > 4000 sq ft selling for < $300k) to improve model generalization.

Feature Selection

    Used a Correlation Matrix to identify the top numeric drivers of price:

        OverallQual (Quality)

        GrLivArea (Size)

        GarageCars (Parking)

        TotalBsmtSF (Basement Size)

        FullBath (Bathrooms)

Feature Engineering

    Imputation: Handled missing values in numeric columns with 0 or median.

    Categorical Encoding: Converted Neighborhood into numerical data using One-Hot Encoding, allowing the model to learn location-based price variance.

3. Machine Learning Models

Two models were trained and evaluated using R² Score and Mean Absolute Error (MAE).

    Linear Regression: A baseline linear model.

    Random Forest Regressor: An ensemble model capable of capturing non-linear relationships between features (e.g., how location impacts price differently depending on house size).

4. Results & Evaluation
Model	R² Score	MAE (Avg Error)
Linear Regression (Baseline)	80.4%	~$24,900
Linear Regression (+ Location)	83.6%	~$22,270
Random Forest (Final Model)	85.9%	~$19,550
Key Findings:

    Adding Neighborhood (Location) improved the Linear model by 3.2%.

    Random Forest outperformed Linear Regression significantly, reducing the average error by another ~$2,700. This suggests that house prices follow non-linear patterns (e.g., Quality matters more in expensive neighborhoods than in cheaper ones).
