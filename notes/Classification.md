# Classification

## Loss function

$y$ Actual value  $\hat{y}$ Predict value

$loss \over residual$ = $y - \hat{y}$

Find the minimum value of $loss \over residual$

- Regression

1. Mean Square Error, MSE (L2 Regularization)

$MSE =$ $1 \over n$$\sum_{i=1}^{n} (y_i- \hat{y_i})^2$

2. Mean Abosolute Error, MAE (L1 Regularization)

$MAE =$ $1 \over n$$\sum_{i=1}^{n} |y_i- \hat{y_i}|$

- Classification

1. Cross-Entropy

see the [Information and Entropy](http://www.ueltschi.org/teaching/chapShannon.pdf)

- Information Gain

$I(x) = -log_2(p(x))$

- Entropy

$H(X) = \sum_{i=1}^{} -p_{i}log_2(p_i)$

- Cross-entropy

$H = \sum_{c=1}^{C}\sum_{i=1}^{n} -y_{c,i}log_2(p_{c,i})$

C is class number, n is the number of data, $y_{c,i}$ is binary indicator (0 or 1) from one hot encode, and $p_{c,i}$ is the probability of i in c class