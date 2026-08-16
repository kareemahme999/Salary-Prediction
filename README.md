# 💰 Salary Prediction using Simple Linear Regression

A simple Machine Learning project that predicts an employee's **salary based on years of experience** using **Simple Linear Regression**.

The project also demonstrates how to evaluate the model and understand the mathematical calculations behind Linear Regression, MSE, R², and variance.

---

## 📌 Project Overview

The goal of this project is to build a Linear Regression model that learns the relationship between:

* **Feature (X):** Years of Experience
* **Target (y):** Salary

The trained model can then predict the expected salary for a given number of years of experience.

---

## 🛠️ Technologies & Libraries

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Jupyter Notebook

---

## 📂 Project Structure

```text
Salary-Prediction/
│
├── salary_prediction.ipynb
├── Salary.csv
└── README.md
```

---

## 🔄 Project Workflow

The notebook follows these steps:

### 1. Load the Dataset

The dataset is loaded using Pandas:

```python
df = pd.read_csv("Salary.csv")
```

### 2. Explore the Dataset

The project checks:

* Dataset shape
* Data information
* Missing values
* First rows of the dataset

### 3. Define Features and Target

```python
X = df[["YearsExperience"]]
y = df["Salary"]
```

Where:

* `X` → Years of Experience
* `y` → Salary

### 4. Train the Model

A `LinearRegression` model from Scikit-learn is created and trained:

```python
regr = LinearRegression()
regr.fit(X, y)
```

The model learns the equation:

```text
y = ax + b
```

Where:

* `a` = coefficient / slope
* `b` = intercept
* `x` = years of experience
* `y` = predicted salary

### 5. Make Predictions

The trained model is used to predict salaries:

```python
y_pred = regr.predict(X)
```

The notebook also predicts the salary for an employee with **4 years of experience**.

### 6. Visualize the Results

The project creates a graph containing:

* Actual salary data points
* The Linear Regression line

This helps visualize the relationship between experience and salary.

### 7. Evaluate the Model

Two evaluation metrics are calculated:

#### Mean Squared Error (MSE)

```python
mse = mean_squared_error(y, y_pred)
```

MSE measures the average squared difference between the actual and predicted salaries.

#### R² Score

```python
r2 = r2_score(y, y_pred)
```

R² measures how well the model explains the variation in the target variable.

---

## 🧮 Mathematical Implementation

One of the main goals of this project is to understand the mathematics behind the model.

The notebook manually calculates:

* MSE
* R² Score
* Predictions using `y = ax + b`
* Variance

The manually calculated values are compared with the values produced by Scikit-learn to verify that they are approximately equal.

---

## 📊 Model Evaluation

The notebook reports:

```text
Coefficient
Intercept
MSE
R² Score
```

It also verifies the manual calculations using NumPy and compares them with Scikit-learn's results.

---

## 🎯 Example Prediction

The trained model is used to predict the salary for:

```text
4 Years of Experience
```

The prediction is generated using:

```python
regr.predict([[4]])
```

---

## 📈 Visualization

The project visualizes the relationship between:

```text
Years of Experience ↔ Salary
```

using a scatter plot and the fitted regression line.

---

## 🎓 What I Learned

Through this project, I practiced:

* Loading and exploring datasets with Pandas
* Working with NumPy
* Understanding Features and Targets
* Training a Linear Regression model
* Making predictions
* Data visualization with Matplotlib
* Evaluating ML models
* Understanding MSE and R²
* Calculating MSE and R² manually
* Understanding the Linear Regression equation
* Calculating variance manually

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <YOUR_REPOSITORY_URL>
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

### 3. Open the notebook

```bash
jupyter notebook salary_prediction.ipynb
```

Make sure `Salary.csv` is located in the same directory as the notebook.

---

## 📌 Future Improvements

Possible improvements for this project include:

* Splitting the dataset into training and testing sets
* Comparing training and testing performance
* Adding more features for salary prediction
* Trying other regression algorithms
* Deploying the model as a simple web application

---

## 👨‍💻 Author

**Kareem Ahmed**

Computer Science Student
Cairo University – Faculty of Computers and Artificial Intelligence

---

⭐ If you found this project useful, feel free to give it a star!
