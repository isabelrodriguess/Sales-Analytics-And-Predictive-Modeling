This project aims to provide actionable insights into sales performance through data analysis and machine learning. It is divided into two parts: Exploratory Data Analysis (EDA) and Sales Quantity Prediction using Machine Learning. The goal is to uncover trends, predict future sales quantities, and provide businesses with the ability to optimize inventory, marketing strategies, and operational decisions.

Project Overview
The project leverages historical sales data to uncover patterns in sales performance across various regions, product categories, customer types, and sales channels. By using machine learning models, the project aims to predict future sales quantities, enabling businesses to make data-driven decisions.

Part 1: Exploratory Data Analysis (EDA)
In Part 1, historical sales data was analyzed to uncover valuable insights into various aspects of the sales process, including:
Monthly sales fluctuations and trends
Regional sales performance and best-performing regions
Product category analysis to identify the highest and lowest sales categories
Impact of discount strategies on sales performance
Customer behavior, comparing new vs. returning customers
Performance of sales channels (online vs. retail)
Seasonal sales patterns and their impact

The analysis found that 22% was the most effective discount rate, and returning customers preferred Furniture products, while Clothing was more popular with new customers. Additionally, the data showed that retail sales dominated in some regions, whereas online sales were more significant in others.
These insights were used to guide business strategy, such as identifying profitable regions, optimizing discount strategies, and tailoring marketing efforts based on customer behaviors and preferences.

Part 2: Sales Quantity Prediction using Machine Learning
In Part 2, machine learning models were applied to predict future Quantity Sold, focusing on accuracy and reliability to assist businesses in planning and decision-making. The models tested include:
Linear Regression: Used as a baseline for prediction, assuming a linear relationship between features and the target variable, Quantity Sold.
Polynomial Regression: Applied to capture non-linear relationships between the features and Quantity Sold.
Random Forest Regression: An ensemble method that combines multiple decision trees to make more robust predictions.

Data Preprocessing
Before training the models, the data underwent extensive preprocessing to ensure it was ready for machine learning:
Feature Selection: The target variable, Quantity Sold, was selected for prediction. Relevant features such as Region, Product Category, Customer Type, Sales Channel, and Month were chosen for the model.
Categorical Encoding: Categorical variables like Region and Product Category were one-hot encoded to allow the models to process them effectively.
Data Split: The dataset was split into 80% for training and 20% for testing, ensuring the models were trained on a portion of the data while evaluated on a separate set for performance.

Model Results
Linear Regression:
R²: 0.738 (indicating the model explained 73.8% of the variance in Quantity Sold)
MSE: 51.60
MAE: 5.35

Polynomial Regression:
R²: 0.852
MSE: 29.20
MAE: 3.68
Random Forest Regression:
R²: 0.969 (showing that the model explained 96.9% of the variance in Quantity Sold)
MSE: 6.09
MAE: 1.44

The Random Forest model was the most accurate, capturing complex patterns in the data and significantly outperforming both linear and polynomial regression models. The model's R² score of 0.969 and its low MSE and MAE demonstrate its ability to make reliable predictions for future sales.

Cross-Validation Results
Cross-validation was performed to evaluate the model's stability across multiple folds. The Random Forest model showed consistently high performance with an average R² score of 0.977, confirming its ability to generalize well to unseen data.

Conclusion
This project demonstrates the effectiveness of machine learning for predicting Quantity Sold. By using Random Forest Regression, businesses can forecast future sales quantities with high accuracy. This allows for better inventory management, more effective marketing strategies, and improved operational planning. The insights gained from EDA also provide valuable business intelligence, helping organizations optimize sales strategies and enhance customer targeting.

Technologies Used
Python
Pandas
Numpy
Scikit-learn
Matplotlib
Seaborn
