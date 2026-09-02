#  Health Insurance Charges Prediction

A Machine Learning project that predicts **health insurance charges** based on personal and demographic factors such as age, BMI, gender, number of children, smoking status, and region.

The project develops and compares **four regression models** and selects the best-performing model based on **Mean Squared Error (MSE)** and **R² Score**.

---

##  Project Overview

Health insurance charges depend on multiple factors, making it difficult to estimate costs manually.

This project uses Machine Learning to build a predictive model that estimates an individual's insurance charges from their input information.

The project compares different regression approaches and identifies the model that performs best on unseen test data.

---

##  Objective

The main objectives of this project are:

* Analyze the health insurance dataset
* Perform data cleaning and exploratory data analysis
* Convert categorical variables into numerical form
* Split the dataset into training and testing sets
* Develop multiple regression models
* Evaluate models using MSE and R² Score
* Select the best-performing model
* Predict insurance charges for new users

---

##  Dataset

The dataset contains **1,338 records** and **7 columns**.

### Features

| Feature    | Description                        |
| ---------- | ---------------------------------- |
| `age`      | Age of the individual              |
| `sex`      | Gender of the individual           |
| `bmi`      | Body Mass Index                    |
| `children` | Number of children/dependents      |
| `smoker`   | Whether the individual is a smoker |
| `region`   | Residential region                 |
| `charges`  | Medical insurance charges (Target) |

### Target Variable

`charges`

---

##  Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab

---

##  Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas
2. Checked the dataset structure and data types
3. Checked for duplicate records
4. Removed duplicate rows
5. Performed exploratory data analysis
6. Converted categorical variables using **One-Hot Encoding**
7. Separated features (`X`) and target (`y`)
8. Split the data into training and testing sets

### Train-Test Split

* Training data: **70%**
* Testing data: **30%**
* random_state = 42

---

##  Machine Learning Models

Four regression models were developed and evaluated.

### Model 1 — Linear Regression (Age Only)

This model uses only the `age` feature to predict insurance charges.

### Model 2 — Linear Regression (Age + BMI)

This model uses:

* Age
* BMI

to improve the prediction compared with Model 1.

### Model 3 — Linear Regression (All Features)

This model uses all available encoded features:

* Age
* BMI
* Children
* Gender
* Smoking status
* Region

### Model 4 — Random Forest Regression 

The fourth model uses **Random Forest Regression** with all available features.

Random Forest was added to capture more complex relationships between the input features and insurance charges.

---

## 📈 Model Evaluation

The models were evaluated using:

### Mean Squared Error (MSE)

MSE measures the average squared difference between actual and predicted values.

**Lower MSE indicates better performance.**

### R² Score

R² measures how well the model explains the variation in the target variable.

**Higher R² indicates better performance.**

---

##  Model Comparison

| Model                       |     Train MSE |   Train R² |       Test MSE |    Test R² |
| --------------------------- | ------------: | ---------: | -------------: | ---------: |
| Model 1 – Age Only          |   134,251,800 |     0.0834 |    131,661,400 |     0.1020 |
| Model 2 – Age + BMI         |   130,289,400 |     0.1105 |    127,364,800 |     0.1314 |
| Model 3 – All Features      |    37,730,550 |     0.7424 |     33,780,510 |     0.7696 |
| **Model 4 – Random Forest** | **3,468,444** | **0.9763** | **21,646,630** | **0.8524** |

---

##  Best Model

### Random Forest Regression

Random Forest Regression achieved the best performance among the four models.

* **Test MSE:** 21,646,630
* **Test R²:** 0.8524

Compared with the Linear Regression model using all features:

* Model 3 Test R²: **0.7696**
* Model 4 Test R²: **0.8524**

Therefore, **Random Forest Regression was selected as the final model** for predicting health insurance charges.

The model explains approximately **85.24% of the variation** in insurance charges on the test data.

---

##  Prediction

The final Random Forest model can be used to predict insurance charges for new users based on their:

* Age
* BMI
* Number of children
* Gender
* Smoking status
* Region

Example output:

```text
Predicted Charges: $XXXXX.XX
```

---

##  Project Structure

```text
Health-Insurance-Charges-Prediction/
│
├── Health Insurance Prediction.ipynb
├── insurance_prediction.csv
└── README.md
```

---

##  Future Scope

* Perform hyperparameter tuning for Random Forest
* Compare additional regression algorithms
* Improve model performance
* Build an interactive prediction interface
* Deploy the model using Streamlit or Flask
* Enable real-time insurance charge prediction

---

##  Key Learning Outcomes

Through this project, I learned:

* Data preprocessing
* Exploratory Data Analysis
* One-Hot Encoding
* Train-Test Splitting
* Linear Regression
* Random Forest Regression
* Model evaluation using MSE and R²
* Comparing multiple Machine Learning models
* Selecting the best model based on test performance

---

## 👩‍💻 Author

**Jessima Afrin**

Machine Learning Project — Health Insurance Charges Prediction
