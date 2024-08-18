# Breast-Cancer-Analysis-and-Prediction-using-Machine-Learning-Algorithms

![image](https://github.com/user-attachments/assets/b48f6b3f-2a58-47e5-a185-1774f8264b54)

### **Breast Cancer: An Overview** 

Breast cancer is a kind of cancer that begins as a growth of cells in the breast tissue.

After skin cancer, breast cancer is the most common cancer diagnosed in women in the United States. But breast cancer doesn't just happen in women. Everyone is born with some breast tissue, so anyone can get breast cancer.

Breast cancer survival rates have been increasing. And the number of people dying of breast cancer is steadily going down. Much of this is due to the widespread support for breast cancer awareness and funding for research.

Advances in breast cancer screening allow healthcare professionals to diagnose breast cancer earlier. Finding the cancer earlier makes it much more likely that the cancer can be cured. Even when breast cancer can't be cured, many treatments exist to extend life. New discoveries in breast cancer research are helping healthcare professionals choose the most effective treatment plans 


There are two types of breast cancer tumors: those that are non-cancerous, or ‘benign’, and those that are cancerous, which are ‘malignant’.

**Benign Tumors**
When a tumor is diagnosed as benign, doctors will usually leave it alone rather than remove it. Even though these tumors are not generally aggressive toward surrounding tissue, occasionally they may continue to grow, pressing on other tissue and causing pain or other problems. In these situations, the tumor is removed, allowing pain or complications to subside.

**Malignant tumors**
Malignant tumors are cancerous and may be aggressive because they invade and damage surrounding tissue. When a tumor is suspected to be malignant, the doctor will perform a biopsy to determine the severity or aggressiveness of the tumor.

## Dataset Overview

Source: Available via UW CS ftp server: ftp://ftp.cs.wisc.edu/math-prog/cpo-dataset/machine-learn/WDBC/ UCI Machine Learning Repository: Breast Cancer Wisconsin (Diagnostic) Dataset

Description: Features computed from digitized FNA images of breast masses, describing characteristics of cell nuclei. Based on 3-dimensional space described in: K. P. Bennett and O. L. Mangasarian (1992).

**Attribute Information:**

- ID number
- Diagnosis (M = malignant, B = benign)
- Ten real-valued features are computed for each cell nucleus:
- radius (mean of distances from center to points on the perimeter)
- texture (standard deviation of gray-scale values)
- perimeter
- area
- smoothness (local variation in radius lengths)
- compactness (perimeter^2 / area - 1.0)
- concavity (severity of concave portions of the contour)
- concave points (number of concave portions of the contour)
- symmetry
fractal dimension ("coastline approximation" - 1)
Feature Values: Recoded with four significant digits. Missing Attribute Values: None reported.

**Class Distribution:**

- 357 benign cases
- 212 malignant cases

## Steps to Build the Prediction Model:

1-Data Preprocessing: -Handle categorical variables (e.g., Breast, Breast Quadrant, Diagnosis Result). -Normalize or scale numerical variables if necessary. -Split the data into training and testing sets.

2-Feature Selection: Select relevant features that contribute most to the prediction. Consider using techniques like correlation analysis or feature importance from tree-based models.

3-Model Selection: -Choose appropriate machine learning algorithms (e.g., Logistic Regression, Decision Tree, Random Forest, Support Vector Machine). -Train multiple models and compare their performance.

4-Model Training and Evaluation: -Train the selected models on the training data. -Evaluate model performance using metrics such as accuracy, precision, recall, F1-score, and ROC-AUC score.

5-Hyperparameter Tuning: -Optimize model parameters using techniques like grid search or random search to improve performance.

6-Model Deployment: -Once the best model is selected, deploy it for predicting new data. -Ensure the model is robust and can handle real-world data.

Exploring This Dataset Can Help With: 
- 📊 Medical Analysis: Understanding the factors influencing breast cancer diagnoses and outcomes.
- 🩺 Clinical Decision-Making: Providing insights to help healthcare professionals in diagnosing and treating breast cancer.
- 📈 Trend Identification: Analyzing trends in breast cancer characteristics and patient demographics.
- 🔍 Research: Offering a robust data foundation for research in oncology and patient care. This dataset is an invaluable resource for anyone looking to develop predictive 
      models for breast cancer, providing a detailed look at the factors influencing diagnosis and patient outcomes.

### EDA: Exploratory Data Analysis

![image](https://github.com/user-attachments/assets/fe73f047-00ca-4168-b9b8-a97448cb4741) ![image](https://github.com/user-attachments/assets/5eefb573-eea7-4a64-88b8-bea59acb9720)

![image](https://github.com/user-attachments/assets/ca3fab51-13f2-4115-af40-17f74f9a80e2)

![image](https://github.com/user-attachments/assets/388aef84-6b2f-4eaa-9994-ee3bf8c5df3e)

![image](https://github.com/user-attachments/assets/5692ba8f-944d-4bd1-acd6-0e33da978128)


Observations: The last column named "Unaname: 32" seems like an erronous coloumn in our dataset. We might probably just drop it. Most of the columns seem to have a numeric entry. This would save our time from mapping the variables. The ID column would not help us contributing to predict about the cancer. We might as well drop it.

Observations: Only the 'diagnosis' column, which we have to predict is of object datatype. There's only ID column of int type. We will probably drop it anyway. There are a total of 31 columns which are of float datatype.

Observations: The following columns are the one's that show the greatest correlation with our diagnosis column. There are two things that can be done. We can either use only the columns which have greatest correlation, or we can continue to use all the columns. I will be using all these columns to predict our result You can eliminate a few and see if the accuracy improves!

Observations: Looks wonderful, isn't it! There are only a handful of columns that show negative correlation with the 'diagnosis column' Around half of our columns are more than 50% positively correlated to diagnosis column. We have to select which of the attributes we want to use in building our model!

The model heavily relies on features like radius_mean and concavity_worst to make predictions, indicating their critical role in breast cancer diagnosis.

Breast cancer diagnosis can be predicted with roughly 97% accuracy using these 30 histological tumor characteristics.

EDA Summary During our data visualization, we found that our dataset contains 569 rows and 32 columns with a total of 18208 datapoints. Out of the 32 columns, we dropped one column that contains only missing values and does not hold any informative value. Our dataset does not contain any duplicated rows.

By visualizing the histogram of each variables, we found that only 37% of the samples were malignant and the remaining 63% were benign. Majority of the predictor variables of the dataset exhibits a right tailed distribution.

Checking on the pearson correlation matrix, we found that majority of the features of the dataset were highly correlated. With this issue, we cannot use linear models without careful feature engineering.

The pairplot for the selected features of the breast cancer dataset, colored by the diagnosis (malignant or benign), provides several insights:

Feature Distribution: Each feature's distribution is plotted along the diagonal. These histograms show how the values of each feature are spread out. For instance, you can see that malignant tumors tend to have higher values for features like radius, perimeter, and area.

Feature Relationships: The scatter plots in the off-diagonal panels show the relationships between pairs of features. These plots are useful for identifying patterns, trends, and clusters. For example, there's a visible positive correlation between radius_mean and area_mean, indicating that as the radius increases, the area tends to increase as well.

Differences Between Diagnoses: The different colors clearly demonstrate how the feature values differ between benign and malignant cases. Malignant cases often have higher feature values, pointing towards larger and more irregular tumors.

Data Distribution: The distribution of data points in these plots also provides insight into the variance and spread of the data. Tight clusters indicate less variation within that diagnosis for a particular feature, while more spread out points indicate greater variation.

Overall, these pairplots are a powerful tool for understanding the relationships between different features and how they relate to the diagnosis of breast cancer. They can also guide further analysis, such as feature selection for machine learning models.

The table presents the performance metrics of four different classification models on a test dataset. These metrics include Precision, Recall, F1-Score, and Accuracy. Here's a brief explanation of each model's performance:

Logistic Regression: Precision: 95.6% Recall: 95.6% F1-Score: 95.6% Accuracy: 95.6% Logistic Regression performs exceptionally well with very high precision, recall, F1-score, and accuracy, indicating a strong ability to correctly classify and balance between positive and negative classes.

Decision Tree: Precision: 91.1% Recall: 91.1% F1-Score: 91.1% Accuracy: 91.1% The Decision Tree shows good performance, but it is slightly lower than Logistic Regression, suggesting it might not be as effective in balancing false positives and false negatives.

SVM: Precision: 97.0% Recall: 97.0% F1-Score: 97.0% Accuracy: 97.7%

KNN: Precision: 94.1% Recall: 94.1% F1-Score: 94.1% Accuracy: 94.1%

XGBoost: Precision: 95.6% Recall: 95.6% F1-Score: 95.6% Accuracy: 95.6% XGBoost, another ensemble method, suggesting its effectiveness in handling complex patterns in the data.

In summary, all models perform well, with SVM showing the best overall metrics. The choice between these models should consider not just these metrics but also the specific context of the problem, such as the cost of false positives vs. false negatives, the complexity of the model, and the computational resources available.


