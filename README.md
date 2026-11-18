# 🎓 Student Score Prediction Using Machine Learning

## 📌 Project Overview

This project was developed as part of the **Elevvo Machine Learning Internship – Machine Learning Track**.

The objective is to predict students' examination scores using machine learning techniques, particularly Linear Regression.

The project explores how different student-related factors, including study hours, attendance, previous academic performance, sleep habits, and other personal and educational characteristics, influence exam score predictions.

Three Linear Regression models were developed and compared to evaluate the impact of using different numbers and types of features.

## 🎯 Objectives

- Explore and understand student performance data.
- Perform data cleaning and exploratory data analysis (EDA).
- Investigate relationships between student characteristics and examination scores.
- Develop a Simple Linear Regression model.
- Develop a Multiple Linear Regression model.
- Apply categorical feature encoding and missing-value imputation.
- Compare model performance using evaluation metrics.
- Analyze prediction errors and model limitations.

## 📂 Dataset

**Dataset:** Student Performance Factors

**Source:** [Student Performance Factors – Kaggle](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors)

Dataset information:
- Total records: 6,607
- Total columns: 20
- Numerical features: 6
- Categorical features: 13
- Target variable: `Exam_Score`

### Selected Features

**Numerical features:**
- Hours_Studied
- Attendance
- Previous_Scores
- Sleep_Hours
- Tutoring_Sessions
- Physical_Activity

**Categorical features:**
- Parental_Involvement
- Access_to_Resources
- Extracurricular_Activities
- Motivation_Level
- Internet_Access
- Family_Income
- Teacher_Quality
- School_Type
- Peer_Influence
- Learning_Disabilities
- Parental_Education_Level
- Distance_from_Home
- Gender

**Target variable:** `Exam_Score`

## 🛠️ Technologies and Libraries

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Development environment |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Scikit-learn | Machine learning |
| Linear Regression | Predictive modelling |

## ⚙️ Project Methodology

### 1. Data Loading and Exploration

- Loaded the Student Performance Factors dataset.
- Inspected dataset structure and data types.
- Examined statistical distributions.
- Identified missing values and duplicate records.

### 2. Data Cleaning

- Identified 235 missing values across three categorical columns.
- Confirmed that there were no duplicate records.
- Used median imputation for missing numerical values.
- Used most-frequent imputation for missing categorical values in the full-feature model.

### 3. Exploratory Data Analysis

- Examined study hours and examination scores.
- Created scatter plots.
- Calculated Pearson correlation.
- Investigated unusual examination scores.

The correlation between study hours and examination scores was **0.4455**, indicating a moderate positive linear relationship.

### 4. Train-Test Split

The dataset was divided into:
- Training data: 80%
- Testing data: 20%

The random state was set to 42 to ensure reproducibility.

### 5. Model Development

Three models were developed:

**Model 1 – Simple Linear Regression**

Used only `Hours_Studied` to predict examination scores.

**Model 2 – Multiple Linear Regression**

Used six numerical features to improve prediction performance.

**Model 3 – Full-Feature Linear Regression**

Used all 19 independent features, combining numerical variables and categorical variables.

Categorical variables were transformed using One-Hot Encoding, while missing values were handled through preprocessing pipelines.

## 📊 Model Performance and Results

The three models were evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R².

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Simple Linear Regression | 2.4476 | 3.2948 | 0.2320 |
| Multiple Linear Regression | 1.2659 | 2.2507 | 0.6416 |
| Full-Feature Linear Regression | 0.4524 | 1.8044 | 0.7696 |

### Best Model

The Full-Feature Linear Regression model achieved the strongest overall performance:

- **MAE:** 0.4524
- **RMSE:** 1.8044
- **R²:** 0.7696

The model explained approximately 76.96% of the variation in examination scores in the test dataset.

## 📈 Visualizations

The project includes the following visualizations:

1. Study Hours vs Exam Scores.
2. Correlation analysis.
3. Simple vs Multiple Linear Regression comparison.
4. Actual vs Predicted Examination Scores.
5. Full-Feature Model Residual Distribution.

These visualizations help evaluate relationships between variables and understand model prediction performance.

## 🔍 Error Analysis and Limitations

Residual analysis revealed that the full-feature model performed well for most observations but struggled with a small group of high-performing students.

Among the nine students in the test set with examination scores above 75:

- Average actual score: 87.22
- Average predicted score: 68.70
- Average absolute prediction error: 18.57

This indicates that the model underestimated some exceptional examination scores.

Potential reasons include:
- Limitations of linear modelling.
- Complex relationships between student characteristics.
- Factors not sufficiently represented by the selected features.

Further experiments with nonlinear regression algorithms and alternative machine learning models could help investigate these limitations.

## 🚀 How to Run the Project

### Option 1: Google Colab

1. Download or clone this repository.
2. Open Google Colab.
3. Upload `Student_Score_Prediction.ipynb`.
4. Download the dataset from Kaggle.
5. Upload the CSV dataset when prompted by the notebook.
6. Run all notebook cells sequentially.

### Option 2: Local Environment

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/Elevvo-Task-1-Student-Score-Prediction.git
```

Navigate to the project directory:

```bash
cd Elevvo-Task-1-Student-Score-Prediction
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open and execute `Student_Score_Prediction.ipynb`.

## 📁 Repository Structure

```text
Elevvo-Task-1-Student-Score-Prediction/
│
├── Student_Score_Prediction.ipynb
├── README.md
├── requirements.txt
│
├── images/
│   ├── correlation.png
│   ├── model_comparison.png
│   ├── actual_vs_predicted.png
│   └── residual_analysis.png
│
└── dataset/
    └── README.md
```

The original dataset is available through the Kaggle source linked above.

## 🔮 Future Improvements

- Experiment with Random Forest Regression.
- Explore Decision Tree Regression.
- Test Polynomial Regression.
- Investigate feature importance.
- Improve predictions for high-performing students.
- Perform cross-validation and hyperparameter tuning.

## 🎓 Internship Information

**Program:** Elevvo Machine Learning Internship

**Track:** Machine Learning

**Task:** Task 1 – Student Score Prediction

**Organization:** Elevvo

**Environment:** Google Colab

## 👨‍💻 Author

**Stewart Daniel**

MSc Applied Informatics  
Vytautas Magnus University, Lithuania

Interested in Artificial Intelligence, Machine Learning, Natural Language Processing, and Data Science.

---

*Developed as part of the Elevvo Machine Learning Internship to gain practical experience in data analysis, predictive modelling, and machine learning evaluation.*

#MachineLearning #Python #LinearRegression #DataScience #Elevvo #ArtificialIntelligence
