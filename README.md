# House Price Prediction using Machine Learning

This project demonstrates a complete workflow for predicting house sale prices using a dataset of residential home features. The entire process, from data exploration and preprocessing to model training and evaluation, is implemented in a single Python script. The project compares the performance of several base and ensemble machine learning models to identify the most effective one for this prediction task.

---

## 📊 Project Workflow

The project follows these key steps:

1.  **Data Loading & Initial Exploration**:
    * The `HousePricePrediction.xlsx` dataset is loaded using `pandas`.
    * Initial analysis includes checking the dataset's shape, data types, and identifying categorical vs. numerical features.

2.  **Exploratory Data Analysis (EDA)**:
    * A **correlation heatmap** is generated to visualize the relationships between numerical features.
    * The number of unique values for each categorical feature is plotted to understand their complexity.
    * The distribution of values for each categorical feature is visualized using bar plots.

3.  **Data Preprocessing**:
    * The `Id` column is dropped as it is not a predictive feature.
    * Missing values in the target variable (`SalePrice`) are filled with the mean.
    * Rows with any remaining missing values are dropped to create a clean dataset.
    * Categorical features are transformed using **One-Hot Encoding** to convert them into a numerical format suitable for machine learning models.

4.  **Model Training & Evaluation**:
    * The dataset is split into training (80%) and validation (20%) sets.
    * Several machine learning models are trained on the data.
    * The performance of each model is evaluated using **Mean Absolute Percentage Error (MAPE)** and **Mean Absolute Error (MAE)**.

---

## 🤖 Models Implemented

The following regression models were trained and compared:

#### Base Models
* Support Vector Machine (SVR)
* Random Forest Regressor
* Linear Regression
* Decision Tree Regressor

#### Ensemble Methods
* **Bagging**: Using Decision Trees as base estimators.
* **Gradient Boosting**: An iterative method that builds strong models from weak ones.
* **AdaBoost**: A boosting algorithm that focuses on correcting the mistakes of its predecessors.

---

## 🛠️ Key Libraries Used

* **pandas**: For data manipulation and analysis.
* **matplotlib** & **seaborn**: For data visualization.
* **scikit-learn**: For data preprocessing, model implementation, and evaluation.

---

## 🚀 How to Run

To run this project on your local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```

2.  **Install the required libraries:**
    *It is recommended to use a virtual environment.*
    ```bash
    pip install pandas matplotlib seaborn scikit-learn openpyxl
    ```

3.  **Place the dataset:**
    Ensure the `HousePricePrediction.xlsx` file is in the same directory as the Python script.

4.  **Execute the script:**
    ```bash
    python your_script_name.py
    ```

The script will print the analysis results and model performance metrics to the console and display the generated plots.
