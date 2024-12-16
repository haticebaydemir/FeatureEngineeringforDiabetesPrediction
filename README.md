# FeatureEngineeringforDiabetesPrediction
# Diabetes Prediction Project
## Overview
This project is aimed at building a classification model to predict diabetes using a dataset, with a strong focus on Feature Engineering. The goal is to enhance the predictive power of the model by transforming raw features into more meaningful and impactful variables. This approach demonstrates the power of feature engineering in improving model performance, through the process of data cleaning, feature creation, and evaluation of the results.

## Libraries 
The following Python libraries were used throughout the project:

- **NumPy**: Numerical operations
- **Pandas**: Data manipulation
- **Matplotlib**: Visualization
- **Seaborn**: Advanced visualization
- **Scikit-learn**: Modeling and evaluation metrics
- **Warnings**: Warning management


## Project Steps and Feature Engineering Process
### 1. Dataset Loading and Initial Inspection
Initially, the diabetes dataset is loaded, and an initial examination of the data is performed. Missing values, outliers, and the distribution of variables are observed. This first step helps in gaining an understanding of the dataset's structure and identifying potential areas that could be improved.
### 2. Exploratory Data Analysis (EDA) and Preprocessing
#### Examination of Categorical and Numerical Variables
The dataset's numerical and categorical variables are separated, and their distributions are analyzed. Categorical variables are visualized, and the basic statistics of numerical variables are summarized, which aids in better understanding the data structure.

#### Handling Missing Data and Outliers
Missing values are imputed using the median, and zero values are replaced with NaN where necessary. Outliers are handled using the interquartile range (IQR) method and capping, where extreme values are limited to a set range. This ensures that erroneous data points do not negatively affect the model.

### 3. Feature Engineering
The feature engineering process is a key focus of this project. Below are the steps taken to create new, informative features that improve model performance:
#### Creation of New Categorical Features
New categorical variables are derived from existing numerical features. This transformation turns numerical values into meaningful categories, improving the model's ability to learn complex patterns.

- **Age Categories**: The age feature is segmented into age ranges like "20-30", "30-40", "40-50", creating a new categorical feature.
- **BMI Categories**: Body Mass Index (BMI) is divided into categories such as "Underweight", "Normal", "Overweight", based on standard BMI ranges.
- **Glucose Categories**: Glucose levels are categorized into "Low", "Normal", and "High".
These categorical variables help the model interpret the data in more context-specific ways, aiding in better prediction of diabetes.

#### Cross-Relationships Between Numerical Features
- **Age and BMI**: A cross-feature combining age and BMI is created to represent the interaction between these two variables. For instance, the combination of specific age ranges and BMI categories adds another layer of detail.
- **Glucose and Age**: A combined feature of age and glucose is created to capture the relationship between these two factors, which are critical in diabetes prediction.
These engineered features improve the model's capacity to detect important patterns by providing additional context and interactions between variables.

#### Data Encoding and Normalization
- **Label Encoding**: Categorical variables are encoded into numerical formats to ensure that they are usable by the model.
- **Feature Scaling**: Numerical data is normalized to a standard range, ensuring that all features contribute equally to model performance.

### 4. Modeling and Result Comparison
**Model Selection: Random Forest Classifier**
After feature engineering, a Random Forest Classifier is selected due to its robustness, ability to handle both numerical and categorical data, and resilience to overfitting.

**Training and Test Set Split**
The dataset is split into 70% for training and 30% for testing. The model is trained on the training data and evaluated on the test data to assess its generalization capability.

**Model Evaluation**
The model's performance is evaluated using several metrics:
- **Accuracy**: 0.77
- **Recall**: 0.706
- **Precision**: 0.59
- **F1 Score**: 0.64
- **AUC (Area Under Curve)**: 0.75
These metrics are critical for evaluating a model in the context of diabetes prediction, where it is crucial to balance precision and recall to minimize false positives and false negatives.

### 5. Feature Importance
The **Feature Importance** method, a built-in capability of the Random Forest algorithm, is used to determine which features most influence the model’s predictions. Analysis reveals that features like glucose levels, age, and BMI have the most significant impact on the model’s decisions, aligning with domain knowledge that these factors are key indicators for diabetes.

## Results: The Impact of Feature Engineering
Feature Engineering has played a critical role in improving model performance. By creating new categorical features and identifying cross-feature relationships, the model is able to make more informed and accurate predictions. Specifically, the combinations of glucose and age, as well as BMI and age, have been shown to be crucial in the model’s decision-making process.

**Two Separate Results Analysis**:

- **Pre-feature engineering model**: A model trained on raw, untransformed data showed a lower accuracy and less reliable results. This was due to the lack of deeper context in the features, which hindered the model's learning process.
- **Post-feature engineering model**: After creating new features, the model achieved higher accuracy and more balanced metrics (precision and recall). This demonstrates the powerful effect of feature engineering on model performance, highlighting its role in producing more reliable diabetes predictions.

## Kaggle Linki 
Projenin detaylarına ve veri setine ulaşmak için: [https://www.kaggle.com/code/haticebaydemir/large-scale-fish-classification]([https://www.kaggle.com/code/haticebaydemir/large-scale-fish-classification-99-6accuracy?scriptVersionId=203133824](https://www.kaggle.com/code/haticebaydemir/featureengineeringfordiabetesprediction))

## İletişim 
Herhangi bir soru veya öneriniz varsa, lütfen benimle iletişime geçin. Proje ile ilgili geri bildirimleriniz benim için değerlidir.

E-posta: baydemirhatice@hotmail.com

Linkedln: https://www.linkedin.com/in/haticebaydemir/
