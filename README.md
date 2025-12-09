# 💰 Data Science Salary Prediction Project

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Muhammad_Hammad-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hammadrehmani/)
[![Kaggle](https://img.shields.io/badge/Kaggle-Muhammad_Hammad-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)](https://www.kaggle.com/hammadrehmani)
[![GitHub](https://img.shields.io/badge/GitHub-Muhammad_Hammad-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/hammadrehmani)
![Python](https://img.shields.io/badge/Python-3.7+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-Deployed-000000?style=for-the-badge&logo=flask&logoColor=white)

#### Hi there! Welcome to my End-to-End Data Science Project.

<p align="center">
  <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=1200&q=80" alt="Data Science Salary Prediction Project" width="100%" height="350">
</p>

> _"It's how you deal with failure that determines how you achieve success."_

---

## 🚩 Table of Contents
- [Project Overview](#-project-overview)
- [Technologies & Resources](#-technologies--resources)
- [Web Scraping Implementation](#-web-scraping-implementation)
- [Data Cleaning & Feature Engineering](#-data-cleaning--feature-engineering)
- [Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [Model Building & Evaluation](#-model-building--evaluation)
- [Model Deployment (Productionization)](#-model-deployment-productionization)
- [About the Author](#-about-the-author)

---

## 📖 Project Overview
* **Goal:** To build a machine learning tool that estimates data science salaries **(MAE ~ $11K)** to assist professionals in negotiating their income.
* **Methodology:** This project covers the full Data Science lifecycle: gathering data via **web scraping**, performing **feature engineering**, training **Regression models**, and deploying a client-facing **API**.
* **Key Results:** The Random Forest model achieved the highest accuracy, outperforming Linear and Lasso Regression baselines.

---

## 📦 Technologies & Resources

| Category | Tools & Libraries |
| :--- | :--- |
| **Language** | Python 3.7+ |
| **Data Processing** | `Pandas`, `NumPy` |
| **Machine Learning** | `Scikit-Learn` (Linear Regression, Lasso, Random Forest, GridSearchCV) |
| **Web Scraping** | `Selenium` (Chrome WebDriver) |
| **Visualization** | `Matplotlib`, `Seaborn` |
| **Deployment** | `Flask`, `Pickle`, `JSON` |

**Resources:**
* **Scraper Repo:** [Glassdoor Selenium Scraper](https://github.com/arapfaik/scraping-glassdoor-selenium)
* **Tutorial:** [Productionizing ML with Flask](https://towardsdatascience.com/productionize-a-machine-learning-model-with-flask-and-heroku-8201260503d2)

---

## 🕷️ Web Scraping Implementation
To create a custom dataset, I utilized **Selenium** to scrape over **1,000 job descriptions** from Glassdoor. 

**Data Points Collected:**
* Job Title & Salary Estimate
* Job Description (Text Data)
* Company Rating, Size, & Founded Date
* Location & Headquarters
* Industry, Sector, Revenue & Competitors

---

## 🧹 Data Cleaning & Feature Engineering
Raw data is rarely usable. I performed extensive data cleaning and engineered new features to quantify the value of specific technical skills.

1.  **Salary Parsing:** Extracted numeric salary data; handled hourly wages and employer-provided estimates.
2.  **Missing Value Handling:** Removed rows with null salary data to ensure target variable integrity.
3.  **Company Age:** Calculated company age from the "Founded Date".
4.  **Skill Parsing (NLP):** Created binary features by parsing job descriptions for high-demand skills:
    * **Python**
    * **R**
    * **Excel**
    * **AWS**
    * **Spark**
5.  **Metadata Extraction:** Simplified job titles (e.g., mapping "Sr. Data Scientist" to "Senior") and calculated job description length.

---

## 📊 Exploratory Data Analysis (EDA)
I conducted EDA to understand the distribution of salaries and the correlation between variables.

| Salary by Job Title | Job Opportunities by State | Feature Correlations |
| :---: | :---: | :---: |
| ![Salary by Title](https://github.com/hammadrehmani/Data-Science-Job-Salary-Prediction-End-to-End/blob/main/salary_by_job_title.PNG) | ![Jobs by State](https://github.com/hammadrehmani/Data-Science-Job-Salary-Prediction-End-to-End/blob/main/positions_by_state.jpg) | ![Correlations](https://github.com/hammadrehmani/Data-Science-Job-Salary-Prediction-End-to-End/blob/main/correlation_visual.jpg) |

---

## 🤖 Model Building & Evaluation
I transformed categorical variables into dummy variables and split the data (80% Train, 20% Test). I implemented three models and evaluated them using **Mean Absolute Error (MAE)** due to its interpretability.

**Models Tested:**
1.  **Multiple Linear Regression:** Used as a baseline.
2.  **Lasso Regression:** Applied for feature selection and normalization due to sparse data.
3.  **Random Forest Regressor:** Selected for its ability to handle non-linear relationships and high dimensionality.

### 🏆 Model Performance
The **Random Forest** model far outperformed the other approaches:

* **Random Forest:** MAE ≈ **11.22** (Best Model)
* **Linear Regression:** MAE ≈ 18.86
* **Ridge Regression:** MAE ≈ 19.67

---

## 🎨 Model Deployment (Productionization)
I built a REST API using **Flask** to serve the model. 
* **Input:** The API accepts a JSON request containing job details (Location, Skills, Industry, etc.).
* **Output:** Returns the predicted salary.
* **Serialization:** The trained model was pickled for efficient loading.

---

## 👤 About the Author

**Muhammad Hammad** *Data Scientist | Machine Learning Enthusiast | Kaggle Contributor*

I am passionate about solving real-world problems using Data Science and AI. Connect with me to discuss this project or potential collaborations.

[![Portfolio](https://img.shields.io/badge/Portfolio-hammadrehmani-000000?style=flat&logo=github&logoColor=white)](https://github.com/hammadrehmani)
[![LinkedIn](https://img.shields.io/badge/Connect-LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hammadrehmani/)
[![Kaggle](https://img.shields.io/badge/Kaggle-Profile-20BEFF?style=flat&logo=kaggle&logoColor=white)](https://www.kaggle.com/hammadrehmani)
