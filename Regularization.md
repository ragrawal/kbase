
# L1 (Lasso)
$$\lambda\sum_i{|\theta_i|}$$

* Helps mititgate the problem of multicollinearity in [[Regression#Ordinary Least Square Regression OLS|Linear Regression]] which commonly occurs in models with large number of parameters*
* 

# L2 (Ridge)
$$\lambda\sum_i{|\theta_i|^2}$$

* Helps mititgate the problem of multicollinearity in [[Regression#Ordinary Least Square Regression OLS|Linear Regression]] which commonly occurs in models with large number of parameters*
* $\lambda$ is a hyperparameter scalar parameter that indicates weight of the regularization 

# Tikhonov Regularization
$$||\Gamma\theta_i||^2_2$$

* Used in [[Matrix Factorization#ALS|ALS]]
* In ridge regression, we use a single weight $\lambda$ to control the influence of regularization. In Tikhonov regularization, we use a N X N matrix, $\Gamma$, where N is the number of parameters. 
* Ridge represession is a special case of Tikhonov regularization where 
	* $$\Gamma = \begin{bmatrix}
 0 & 0 & 0 & \dots \\ 
 0 & \lambda  & 0 & \dots \\ 
 0 &  0 &  \lambda & \dots \\ 
 \dots &  \dots &  \dots & \lambda 
\end{bmatrix}$$ 