Overview
This project focuses on analyzing historical sales data to uncover insights and predict future sales quantities using machine learning. The goal is to help businesses optimize inventory, marketing campaigns, and resources by predicting sales performance across various regions, customer types, and product categories.

The project is divided into two main parts:

Exploratory Data Analysis (EDA) – Exploring sales trends, customer behaviors, and product performance.
Sales Quantity Prediction using Machine Learning – Building and training machine learning models to forecast sales quantities for future periods.
The dataset used for this analysis is from Kaggle and contains variables such as product ID, sale date, region, sales amount, quantity sold, customer type, payment method, and discount rate.

Part 1: Exploratory Data Analysis (EDA)
The exploratory data analysis focused on uncovering key patterns and trends in the sales data. Key insights from the analysis include:

Sales Trends and Regional Performance:
Sales remained relatively stable for the majority of the year but experienced a significant drop in January 2024, likely due to missing data. This highlighted an area for further investigation, potentially related to data inconsistencies or external factors.
East Region consistently outperformed other regions, particularly in product categories like Food and Clothing.
North Region experienced significant struggles, especially in January 2024, where no sales were recorded. This could point to regional marketing challenges or data-related issues.
South Region displayed steady sales and had a strong customer base of returning customers, indicating greater customer loyalty.
The West Region showed inconsistent sales performance but managed to recover towards the end of the year, signaling potential for improvement with the right strategies.

Product Performance:
Certain product categories stood out over the course of the year. Clothing emerged as the top-selling category with steady sales, while Furniture and Food performed particularly well in the East Region. However, sales in Clothing and Furniture dropped sharply in January 2024, pointing to seasonality or external events that might have impacted sales.

Discounts and Customer Behavior:
Discount strategies had varying effects on sales. A 22% discount was identified as the most effective in driving sales, suggesting that businesses should focus on offering discounts within this range to boost revenue.
In terms of customer behavior, new customers slightly outperformed returning customers in terms of revenue. New customer acquisition was particularly strong in the North and East regions, while South and West regions had higher proportions of returning customers, indicating strong brand loyalty in those areas.

Sales Channels:
Sales were fairly split between retail and online channels, with retail sales slightly outperforming online sales overall. However, certain product categories showed channel-specific preferences—Clothing performed better in physical retail stores, while Electronics had stronger sales online.

Key Recommendations:
Focus on offering discounts in the 20%-24% range to maximize sales potential.
Enhance efforts to attract new customers in the South and West regions to complement the existing loyal customer base.
Optimize product offerings for each sales channel, ensuring that Clothing remains retail-focused while Electronics receives more online attention.

Part 2: Sales Quantity Prediction using Machine Learning
The second part of the project focused on leveraging machine learning to predict sales quantities, providing insights into future demand and enabling better business decisions.

Data Preprocessing:
Before training the machine learning models, the data underwent preprocessing to ensure its suitability. Quantity Sold was chosen as the target variable for prediction, while features like Region, Product Category, Customer Type, and Sales Channel were selected as inputs.

Categorical features, such as Region and Product Category, were encoded using One-Hot Encoding to convert them into numerical values that could be processed by machine learning algorithms. The dataset was then split into 80% for training and 20% for testing to evaluate model performance accurately.

Model Selection and Performance:
Three machine learning models were tested for predicting sales quantities:
Linear Regression:
Linear Regression served as a baseline model. While it performed adequately with an R² of 0.738, its simple nature did not capture complex relationships in the data, which led to a higher Mean Squared Error (MSE) of 51.60.

Polynomial Regression:
Polynomial Regression allowed for more flexibility, capturing non-linear relationships between the features and the target variable. The model showed an improved performance, with an R² of 0.852, a reduced MSE of 29.20, and a Mean Absolute Error (MAE) of 3.68.

Random Forest Regression:
The Random Forest model was the standout performer. This ensemble model combined multiple decision trees to capture complex patterns and reduce overfitting. It achieved an impressive R² of 0.969, with a very low MSE of 6.09 and MAE of 1.44. This model demonstrated the highest accuracy and robustness, making it the best choice for future sales predictions.

Cross-Validation:
To ensure the Random Forest model’s stability and generalizability, cross-validation was performed. The model’s R² scores across multiple folds ranged from 0.965 to 0.986, with an average R² of 0.977, confirming that it could be reliably applied to unseen data.

Conclusion:
The Random Forest Regression model emerged as the most accurate and effective method for predicting future sales quantities. Its ability to explain the majority of variance in the data with minimal prediction error makes it a valuable tool for businesses seeking to optimize inventory, marketing strategies, and operations.

Tools and Libraries Used:
Pandas: For data manipulation and analysis.
NumPy: For numerical computations.
Matplotlib & Seaborn: For data visualization.
Scikit-learn: For building and evaluating machine learning models:
RandomForestRegressor and LinearRegression for predictive modeling.
train_test_split, cross_val_score, and PolynomialFeatures for model evaluation and feature transformation.
mean_absolute_error and mean_squared_error for performance metrics.

Final Thoughts:
This project showcases the potential of using machine learning to predict sales quantities with high accuracy. The insights gained from the Exploratory Data Analysis and the Random Forest Regression model provide valuable guidance for improving business operations, enhancing inventory management, and optimizing marketing efforts. By leveraging these insights, businesses can make more informed decisions and stay ahead of future demand trends.
