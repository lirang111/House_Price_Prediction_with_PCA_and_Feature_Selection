# House_Price_Prediction_with_PCA_and_Feature_Selection

🏡 Housing Price Prediction with PCA and Feature Selection
This project applies dimensionality reduction and feature selection techniques to predict housing sale prices using linear regression. The dataset is the classic Ames Housing Dataset, containing 80+ features describing various aspects of residential homes in Ames, Iowa.

📌 Project Goals
Clean and preprocess the housing dataset.

Apply Principal Component Analysis (PCA) to retain 90% of the variance.

Select high-variance features using a variance threshold after Min-Max scaling.

Train and evaluate linear regression models on:

The original feature set

PCA-transformed features

High-variance features only

Compare model performance using R² Score and RMSE.

📂 Dataset

Size: 1460 samples × 81 columns

Target: SalePrice

Data cleaning:

Removed columns with more than 40% missing values

Filled numeric missing values with median

Filled categorical missing values with mode

Converted categorical columns to dummy variables

⚙️ Methods
1. Linear Regression (Baseline)
All features included (after preprocessing and encoding)

R²: ~0.686

RMSE: ~46,892

2. PCA (90% Variance Retained)
Standardized features using StandardScaler

Reduced dimensions from 229 to 124

R²: ~0.838

RMSE: ~33,702

✅ Best performing model

3. High Variance Feature Selection
Scaled features with MinMaxScaler

Selected features with variance > 0.1 (40 features)

R²: ~0.639

RMSE: ~50,317

📊 Results Summary
Model	R² Score	RMSE	Notes
All Features	0.686	46,892	Baseline
PCA (90% variance)	0.838	33,702	Best generalization performance
High-Variance Features	0.639	50,317	Simpler but less accurate model

💡 Key Takeaways
PCA can reduce overfitting and improve generalization by removing noise and redundancy.

High-variance features contribute significantly, but excluding low-variance ones may lose useful information.

Feature selection techniques should be combined for optimal results.

📦 Tools and Libraries
Python (Pandas, NumPy)

Scikit-learn (LinearRegression, PCA, MinMaxScaler, train_test_split)

Jupyter Notebook

📈 Future Improvements
Explore other regression models (e.g., Ridge, Lasso, XGBoost)

Use cross-validation for more robust performance estimates

Incorporate external datasets or domain knowledge

Apply SHAP for interpretability of PCA components



