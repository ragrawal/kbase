**Summary**
* **Ordinary Least Square Regression**: It is a general technique to solve ill-poised problems such as Ax=b where there is no single solution. In such cases, the solution a viable solution is one that minimizes sum of squared error i.e. $||Ax-b||^2_2$.
* **Reguarlized Regression:**
	* **Lasso Regression:** Extends OLS by adding [[Regularization#L1 Ridge|L1]] penalty to nullify effect of correlated features. Helps generate sparse feature sets. 
	* **Ridge Regression**: Extends OLS by adding [[Regularization#L2 Lasso|L2]] penalty to avoid overfitting. It penalizes parameters for taking extreme values and thereby lose generalization. 
	* **Elastic Net Regression**: Extends OLS by adding [[Regularization#L1 Ridge|L1]] and [[Regularization#L2 Lasso|L1]] penalty together. 
* **Spline Regression**: Construct different OLS for different zones of the dataset. 
		
# Ordinary Least Square Regression (OLS)
* $Hypothesis: h_\theta (x) = \theta_0 + \sum_{i=1}^n{\theta_ix_i} = \theta^TX$
* $\text{Cost Function}: J(\theta) = \frac{1}{2m}\sum_{i=1}^m(y-h_\theta(x))^2$

* Note it is assume $x_0 = 1$ so that we can include bias parameter as part of the $\theta$. 
* OLS is a technique in which a straight line is used to estimate the relationship between two interval/ratio variables. The line that minimizes the sum of the squared errors (the distance between the line and each observation) is said to be the "best-fitting line.
* We can minimize the above cost function either using gradient descent or analytical. 
* **Least Square Method**
	* $\theta_j = \theta_j - \frac{\alpha}{m}\sum_{i=1}^m{(y-h_\theta(x))x^i_j}$
	* Note that all parameters are updated simulatenously. i.e. we compute $\sum_{i=1}^m{(y-h_\theta(x))x^i_j}$ first and then perform updates 
	* $\alpha$ is learning rate and controls how far the gradient we want to follow
	* Note that features should be normalized beforehand

| Least Square Method | Analytical Solution |
|------------------------------|---------------------------|
|  | $\theta = (X^TX)^{-1}X^TY$


# Multiple OLS

# Lasso Regression

# Ridge Regression

# Elastic Net Regression

# Spline Regression
