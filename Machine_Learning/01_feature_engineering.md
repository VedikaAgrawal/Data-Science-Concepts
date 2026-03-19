# Machine Learning & Feature Engineering: Assignment Answers

### 1. What is a parameter?
A **parameter** is a configuration variable that is internal to the model and whose value can be estimated from the data. These are the weights and biases that the model "learns" during the training process to make accurate predictions.

---

### 2. What is correlation? What does negative correlation mean?
**Correlation** is a statistical technique that indicates how strongly two variables are related to each other. It measures the degree to which the variables move in relation to one another, typically on a scale from -1 to +1.
**Negative correlation** (or inverse correlation) means that as the value of one variable increases, the value of the other variable decreases. For example, as the speed of a car increases, the time taken to reach a destination decreases.

---

### 3. Define Machine Learning. What are the main components in Machine Learning?
**Machine Learning** is a branch of Artificial Intelligence that enables systems to learn from data and improve from experience without being explicitly programmed. The three main components are:
* **Data:** The input used for learning (Features and Targets).
* **Model/Algorithm:** The mathematical structure that processes the data.
* **Evaluation (Loss Function):** The method used to measure accuracy and guide the learning process.

---

### 4. How does loss value help in determining whether the model is good or not?
The **loss value** represents the "penalty" for a bad prediction. It quantifies the difference between the model's prediction and the actual value. A high loss indicates the model is performing poorly, while a lower loss suggests the model's predictions are becoming more accurate.

---

### 5. What are continuous and categorical variables?
* **Continuous Variables:** These are numeric values that can take any value within a range (e.g., weight, height, temperature, or price).
* **Categorical Variables:** These represent discrete groups or labels (e.g., gender, car brand, or "True/False").

---

### 6. How do we handle categorical variables in Machine Learning? What are the common techniques?
Most Machine Learning models cannot process text, so categorical data must be converted to numbers using **Encoding**. Common techniques include:
* **One-Hot Encoding:** Creates a new binary column (0 or 1) for each unique category.
* **Label Encoding:** Assigns a unique integer (0, 1, 2...) to each category label.

---

### 7. What do you mean by training and testing a dataset?
* **Training:** Using a large portion of the data to let the model learn patterns and adjust its internal parameters.
* **Testing:** Using a separate, unseen portion of the data to evaluate how well the model performs on new information, ensuring it hasn't just "memorized" the training data.

---

### 8. What is sklearn.preprocessing?
**`sklearn.preprocessing`** is a module within the Scikit-Learn library that provides tools for data cleaning and transformation. It includes functions for scaling features, normalizing data, and encoding categorical variables.

---

### 9. What is a Test set?
A **Test set** is a subset of the original data that is set aside and never shown to the model during the training phase. It acts as a final exam to provide an unbiased evaluation of the model's accuracy.

---

### 10. How do we split data for model fitting (training and testing) in Python? How do you approach a Machine Learning problem?
In Python, we use the `train_test_split` function from the `sklearn.model_selection` library. 
**Example:** `X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)` splits the data into 80% training and 20% testing.
A standard approach involves these steps:
1.  **Define the Goal:** Understand what you are trying to predict.
2.  **Data Collection:** Gather the necessary datasets.
3.  **EDA (Exploratory Data Analysis):** Visualize and analyze the data for patterns.
4.  **Feature Engineering:** Handle missing values, scale features, and encode categories.
5.  **Model Selection & Training:** Choose an algorithm and fit it to the data.
6.  **Evaluation:** Test the model and tune it for better performance.

---

### 11. Why do we have to perform EDA before fitting a model to the data?
**Exploratory Data Analysis (EDA)** allows you to understand the data's structure, identify outliers that might ruin predictions, find missing values, and determine which features are most important. Fitting a model without EDA is like driving in a new city without a map.

---

### 12. What is correlation?
**Correlation** is a statistical technique that indicates how strongly two variables are related to each other. It measures the degree to which the variables move in relation to one another, typically on a scale from -1 to +1.

---

### 13. What does negative correlation mean?
**Negative correlation** (or inverse correlation) means that as the value of one variable increases, the value of the other variable decreases. For example, as the speed of a car increases, the time taken to reach a destination decreases.

---


### 14. How can you find correlation between variables in Python?
The easiest way is to use the **`.corr()`** method on a Pandas DataFrame. This generates a correlation matrix. You can also visualize this using a heatmap from libraries like Seaborn.

---

### 15. What is causation? Explain difference between correlation and causation with an example.
**Causation** means that one event is the direct cause of another. 
* **Difference:** Correlation shows that two things move together, but it doesn't mean one caused the other.
* **Example:** There is a correlation between drowning deaths and ice cream sales (both peak in summer). However, eating ice cream doesn't *cause* drowning—the hot weather (the "third variable") causes both.

---

### 16. What is an Optimizer? What are different types of optimizers?
An **Optimizer** is an algorithm that adjusts the model's parameters (weights) to minimize the loss function. 
* **SGD (Stochastic Gradient Descent):** Updates parameters for each training sample.
* **Adam:** An adaptive optimizer that is generally fast and efficient.
* **RMSProp:** Often used in recurrent neural networks to stabilize the learning process.

---

### 17. What is sklearn.linear_model?
**`sklearn.linear_model`** is a Scikit-Learn module that contains algorithms for linear modeling. This includes **Linear Regression** (for predicting continuous numbers) and **Logistic Regression** (for classification tasks).

---

### 18. What does model.fit() do? What arguments must be given?
The **`.fit()`** method starts the training process. It requires two main arguments:
1.  **X:** The input features (the data the model uses to learn).
2.  **y:** The target labels (the answers the model is trying to predict).

---

### 19. What does model.predict() do? What arguments must be given?
The **`.predict()`** method uses the trained model to generate outputs for new, unseen data. It requires one main argument:
1.  **X:** The new input features you want predictions for.

---

### 20. What are continuous and categorical variables?
* **Continuous Variables:** These are numeric values that can take any value within a range (e.g., weight, height, temperature, or price).
* **Categorical Variables:** These represent discrete groups or labels (e.g., gender, car brand, or "True/False").

---

### 21. What is feature scaling? How does it help in Machine Learning?
**Feature scaling** is the process of normalizing the range of independent variables. It helps because many algorithms use "distance" to calculate relationships. If one feature (like "Salary") has much larger numbers than another (like "Age"), the model might wrongly assume the larger numbers are more important.

---

### 22. How do we perform scaling in Python?
Scaling is typically done using classes from `sklearn.preprocessing`:
* **StandardScaler:** Rescales data so the mean is 0 and the standard deviation is 1.
* **MinMaxScaler:** Rescales all data points to fall between a range of 0 and 1.

---
### 23. What is sklearn.preprocessing?
**`sklearn.preprocessing`** is a module within the Scikit-Learn library that provides tools for data cleaning and transformation. It includes functions for scaling features, normalizing data, and encoding categorical variables.

---

### 24. How do we split data for model fitting (training and testing) in Python?
In Python, we use the `train_test_split` function from the `sklearn.model_selection` library. 
**Example:** `X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)` splits the data into 80% training and 20% testing.

---

### 25. Explain data encoding?
**Data encoding** is the process of converting non-numerical data (text/categories) into a numerical format. Since machines only understand numbers, we use encoding (like One-Hot or Label Encoding) to represent categories like "Red," "Blue," and "Green" as 0s and 1s.

