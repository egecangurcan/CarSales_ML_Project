# CarSales_ML_Project

Project Overview
This project aims to predict the selling price of cars with using two types of machine learning algorithms, supervised and unsupervised, on the same dataset. Specifically, a Random Forest Regressor was used for the supervised learning task, and a Random Forest Classifier was used for the unsupervised learning task after a custom transformation of the target variable.

About Dataset
The dataset includes various features, and the target variable is a normalized version of selling prices. For the supervised model, the raw continuous target variable was used, while for the unsupervised model, the target was categorized into three distinct price categories: low, mid, and high based on quartile splits.


Supervised Learning

Algorithm: Random Forest Regressor
Goal: Predict the normalized selling price of products using various features from the dataset.

Steps;
Feature Selection: The Random Forest model was initially trained on all features to determine their importance. The top 250 most important features were selected for final training.
Model Training: A Random Forest Regressor was trained using the top 250 selected features.
Evaluation Metrics: The model's performance was evaluated using the Root Mean Squared Error (RMSE) and the R² score.

Results:
RMSE with top 250 features: 0.0891
R² Score with top 250 features: 0.846
Interpretation:

The supervised learning model performed well, achieving an R² score of 0.846, indicating that about 84.6% of the variance in the selling prices can be explained by the model. The relatively low RMSE (0.0891) indicates a good fit, suggesting that the model can predict prices with reasonable accuracy.


Unsupervised Learning

Algorithm: Random Forest Classifier
Goal: Classify the selling price of products into low, mid, and high categories.

Steps;
Price Categorization: The continuous selling price variable was categorized into three price ranges: low, mid, and high, using the first quartile (Q1) and third quartile (Q3) as thresholds.
Model Training: A Random Forest Classifier was used to predict the price category.
Evaluation Metrics: The model's performance was evaluated using the confusion matrix and classification report (precision, recall, f1-score).

Classification Report:
Precision, Recall, and F1-score for all categories (high, mid, low) were all 1.00.
Overall accuracy: 100%



Comparison and Conclusion

The dataset is more naturally suited for unsupervised classification tasks where clear price groupings (low, mid, high) exist. The Random Forest Classifier achieved perfect results after categorizing the prices, which suggests that the features in this dataset strongly correspond to these price categories.

In contrast, the supervised learning task of predicting continuous price values achieved good performance, but not perfect. The Random Forest Regressor provided a solid predictive model with an R² score of 0.846, but continuous regression tasks are generally harder and more sensitive to small variances in the data.
