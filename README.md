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

Class Distribution:

- 357 benign cases
- 212 malignant cases

Steps to Build the Prediction Model:

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

