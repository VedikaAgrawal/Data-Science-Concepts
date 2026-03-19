# Regression Analysis Assignment

### 1. What is Simple Linear Regression?
Simple Linear Regression is a statistical method used to model the relationship between a single independent variable ($X$) and a dependent variable ($Y$) by fitting a linear equation to observed data.

---

### 2. What are the key assumptions of Simple Linear Regression?
The key assumptions include:
- **Linearity:** The relationship between $X$ and $Y$ is linear.  
- **Independence:** Observations are independent of each other.  
- **Homoscedasticity:** The variance of residual errors is constant across all levels of $X$.  
- **Normality:** The residuals (errors) of the model are normally distributed.  

---

### 3. What does the coefficient $m$ represent in the equation $Y = mX + c$?
The coefficient $m$ represents the slope of the regression line. It indicates the change in the dependent variable ($Y$) for every one-unit increase in the independent variable ($X$).

---

### 4. What does the intercept $c$ represent in the equation $Y = mX + c$?
The intercept $c$ represents the value of $Y$ when $X$ is equal to zero. It is the point where the regression line crosses the Y-axis.

---

### 5. How do we calculate the slope $m$ in Simple Linear Regression?
The slope $m$ is calculated using the formula:

$$
m = \frac{\sum((X_i - \bar{X})(Y_i - \bar{Y}))}{\sum(X_i - \bar{X})^2}
$$

Where $\bar{X}$ and $\bar{Y}$ are the mean values of the variables.

---

### 6. What is the purpose of the least squares method in Simple Linear Regression?
The purpose of the Ordinary Least Squares (OLS) method is to find the best-fitting line by minimizing the sum of the squares of the vertical deviations (residuals) between each data point and the fitted line.

---

### 7. How is the coefficient of determination ($R^2$) interpreted in Simple Linear Regression?
$R^2$ represents the proportion of the variance in the dependent variable that is predictable from the independent variable.  
An $R^2$ of 0.80 means that 80% of the variation in $Y$ is explained by $X$.

---

### 8. What is Multiple Linear Regression?
Multiple Linear Regression is an extension of simple linear regression used to model the relationship between one dependent variable and two or more independent variables.

---

### 9. What is the main difference between Simple and Multiple Linear Regression?
The main difference is the number of independent variables.  
- Simple regression uses one predictor ($X$)  
- Multiple regression uses multiple predictors ($X_1, X_2, ... X_n$)

---

### 10. What are the key assumptions of Multiple Linear Regression?
In addition to the assumptions of simple linear regression:
- Linearity  
- Independence  
- Homoscedasticity  
- Normality  

It also assumes:
- **No Multicollinearity:** Independent variables should not be highly correlated.

---

### 11. What is heteroscedasticity, and how does it affect the results of a Multiple Linear Regression model?
Heteroscedasticity occurs when the variance of errors is not constant across observations.  
It does not bias the coefficients but makes the standard errors unreliable, leading to incorrect p-values and confidence intervals.

---

### 12. How can you improve a Multiple Linear Regression model with high multicollinearity?
Techniques include:
- Removing one of the highly correlated variables  
- Combining correlated variables into a single index  
- Using Principal Component Analysis (PCA)  
- Applying Regularization (Ridge or Lasso regression)  

---

### 13. What are some common techniques for transforming categorical variables for use in regression models?
Common techniques include:
- **One-Hot Encoding** (creating dummy variables)  
- **Label Encoding** (assigning numerical values)  

One-Hot Encoding is generally preferred to avoid implying false order.

---

### 14. What is the role of interaction terms in Multiple Linear Regression?
Interaction terms are used when the effect of one independent variable on the dependent variable depends on another variable.  
They help capture more complex relationships.

---

### 15. How can the interpretation of intercept differ between Simple and Multiple Linear Regression?
- In Simple Regression: Intercept is $Y$ when $X = 0$  
- In Multiple Regression: Intercept is $Y$ when all independent variables are zero  

---

### 16. What is the significance of the slope in regression analysis?
The slope determines the strength and direction of the relationship.  
A steeper slope indicates higher sensitivity of $Y$ to changes in $X$.

---

### 17. How does the intercept provide context in regression?
The intercept provides a baseline value and anchors the relationship between variables.

---

### 18. What are the limitations of using $R^2$ alone?
- Always increases with more variables  
- Does not indicate model bias  
- Does not guarantee good performance on new data  

---

### 19. How would you interpret a large standard error?
A large standard error indicates an imprecise estimate of the coefficient, often suggesting:
- Low significance  
- Possible multicollinearity  

---

### 20. How can heteroscedasticity be identified?
It appears as a **fan or funnel shape** in residual plots.  
It must be addressed for valid hypothesis testing.

---

### 21. What does high $R^2$ but low adjusted $R^2$ indicate?
It suggests **overfitting**, where irrelevant variables inflate $R^2$ without improving the model.

---

### 22. Why is scaling important in Multiple Linear Regression?
Scaling ensures variables with larger numerical ranges do not dominate the model.

---

### 23. What is polynomial regression?
Polynomial Regression models the relationship as an $n^{th}$ degree polynomial.

---

### 24. How does polynomial regression differ from linear regression?
- Linear: $Y = mX + c$ (straight line)  
- Polynomial: Includes terms like $X^2, X^3$ (curved relationships)  

---

### 25. When is polynomial regression used?
When data shows a curved pattern instead of a straight line.

---

### 26. What is the general equation for polynomial regression?

$$
Y = \beta_0 + \beta_1X + \beta_2X^2 + ... + \beta_nX^n + \epsilon
$$

---

### 27. Can polynomial regression be applied to multiple variables?
Yes, it can be extended to multivariate cases with interaction terms.

---

### 28. What are the limitations of polynomial regression?
- **Overfitting:** High-degree models fit noise  
- **Poor extrapolation:** Unreliable outside training range  

---

### 29. How to evaluate polynomial degree?
- Cross-validation  
- Adjusted $R^2$  
- Mean Squared Error (MSE)  

---

### 30. Why is visualization important?
It helps verify whether the curve fits the data properly and detect overfitting.

---

### 31. How is polynomial regression implemented in Python?
Using **Scikit-Learn**:
- Transform features using `PolynomialFeatures`  
- Fit using `LinearRegression`  