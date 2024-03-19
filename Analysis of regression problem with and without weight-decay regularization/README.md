Analysis of regression problem with and without weight-decay regularization


X and Y are both real valued random variables, where X takes value in (0, 1) and Y depends on X according to

Y = cos(2πX) + Z 

where Z is a zero mean Gaussian random variable with variance σ square and Z is independent of X. Based on the observed sample (X,Y) learning a polynomial regression model and examining the fitting and generalization capability of the model in relation to the model complexity and sample size.

Steps:

❼ A function getData was created for generating the (X,Y) of N sample size and noise σ square.

❼ Second function getMSE, which calculate the Mean Square error was created.

❼ Fitting of the given dataset to a polynomial of degree d was done using the function fitData. Here the error was calculated separately for training(Ein) and test data set (Eout)

❼ A function experiment was defined in which for values of N, d and σ square the loops over M trial (50) and thereby calculating average value of both Error, Ein avg and Eout avg.

❼ Running the experiment for all values of N ∈ {2, 5, 10, 20, 50, 100, 200}, d ∈ {1, 2, 4, 8, 16, 32, 64} and σ ∈ {0.05, 0.2}.

❼ Plotting the graph of Ein avg and Eout avg for all sigma values by selecting three values of N ={2, 50, 200} as a function of d.

❼ Plotting the graph of Ein avg and Eout avg for all sigma values by selecting three values of d ={1, 8, 64} as a function of N.

❼ Repeating the experiment by initializing weight decay regularization parameter (λ=0.1) and calculating the gradient and thereby Ein avg and Eout avg and plotting as a function of N and d.


Conclusion:

❼ In machine learning, models tend to overfit when there is limited data that is model fits the noise in the training data, leading to a large gap between training and testing errors.

❼ As the sample size increases, the model is less likely to overfit because there is more data to learn from. As a results there is a reduction in the variance of the model’s predictions and a smaller gap between training and testing errors.

❼ Lower order polynomials tend to have higher bias but lower variance causing the data to underfit sometimes. But for higher order variance is high bt bias is less causing to overfit the mode.

❼ The plot of training and testing error can exhibit oscillatory behavior as you vary the N and d, indicating the complex interplay between these two factors.

❼ It’s crucial to choose an appropriate polynomial degree or use regularization techniques to control model complexity and prevent overfitting when working with polynomial regression.

❼ The optimal level of regularization depends on the specific problem and dataset.Finding the right balance between model complexity and regularization is a crucial part of model tuning. It can help control overfitting, making the model generalize better to unseen data, but finding the right amount of regularization requires experimentation and validation on a separate test set or through cross-validation.
