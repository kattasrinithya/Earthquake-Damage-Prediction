# Earthquake-Damage-Prediction

Overview
This project aims to predict the level of damage sustained by buildings after an earthquake using structured data about building features and location. The model classifies buildings into three damage grades: Low, Medium, and High, helping authorities prioritize structural reinforcements and post-disaster response planning.

Objectives--
Analyze and understand patterns that lead to structural damage.
Build accurate predictive models using machine learning.
Provide actionable insights to improve construction practices and disaster preparedness.

Dataset--
The dataset includes various features such as:
Building geometry (count_floors_pre_eq, height_percentage, etc.)
Material and structural attributes (foundation_type, roof_type, superstructure materials)
Location identifiers (geo_level_2_id)
Secondary use information (has_secondary_use_*)
Target column: damage_grade (1: Low, 2: Medium, 3: High)

##Key Steps
1. Exploratory Data Analysis (EDA)--
Univariate, bivariate, and multivariate visualizations.
Checked class imbalance and feature distributions.

2. Data Preprocessing--
Handled missing values, skewness, and outliers (via Winsorization and IQR).
Applied appropriate encoding: Target Encoding & One-Hot Encoding.
Scaled features using MinMaxScaler (after log-transforming skewed ones).

3. Model Building--
Trained and tuned multiple classifiers:
Logistic Regression
Decision Tree
Random Forest
Gradient Boosting
XGBoost
Used GridSearchCV for hyperparameter tuning.

4. Ensemble Techniques
Built a Stacking Classifier with XGBoost + Random Forest, achieving the highest accuracy.

--Compared model performance using accuracy and classification reports.

Final Results--
Model	Accuracy
Logistic Regression	55.13%
Decision Tree	51.83%
Random Forest	61.35%
Gradient Boosting	59.53%
Tuned XGBoost	63.03%
Stacking Ensemble (XGB + RF)	64.11%

Challenges Faced--
Class Imbalance: Resolved with SMOTE and class weighting.

High Feature Skewness: Corrected using log transformation.

Outliers: Managed using IQR and Winsorization methods.

Encoding Strategy: Carefully selected encoders based on cardinality and model compatibility.

Conclusion--
After extensive preprocessing, feature engineering, and ensemble modeling, the stacking model (XGBoost + Random Forest) delivered the best performance. This solution can be valuable for disaster risk management and infrastructure planning.

Requirements---
Python 3.x
Scikit-learn
XGBoost
Pandas, Numpy, Matplotlib, Seaborn
imbalanced-learn
category_encoders
