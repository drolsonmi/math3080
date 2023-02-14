# Midterm Review
1. Data
    * Categorical
      * Ordinal/Nominal
    * Quantitative Data
      * Discrete/Continuous
    * Big Data vs. Smart Data
    * Stages of Gathering Data
      * Plan (What information do I need?)
      * Gathering the data (Collecting, Curating the data, Cleaning the data...)
      * Analysis of the data (visualization, statistics, models)
      * Explanation of the data (Cleaning and Presenting the visuals with explanations)
        * Tico Bray, Johannes Kepler, Isaac Newton
    * What is a Data Scientist
      * Could include
      * One who studies effective ways to collect, store, analyze, and model data
      * T-model vs. the Pi-model

2. Python
    * Basics of Python
    * Pandas
    * NumPy
    * Summary Statistics in Python

3. Linear Algebra
    * Vectors
    * Basis Vectors
    * Norms
    * Linear Transformation
    $$A\vec{x} = \vec{y}$$
    * Eigenvalues and Eigenvectors
    $$A\vec{x}=\lambda\vec{x}$$
    * Solving for x
    $$A\vec{x}=b\qquad\vec{x}=A^{-1}b$$

4. Statistics (Probability)
    * Probability
    * Sample Spaces
    * Conditional Probability
    * Normal Distributions
    * Expected Values / Variance
    * Joint, Marginal, and Conditional Distributions

5. Linear Regression and Errors
    * Covariance
    * Correlation
    * 2-D Linear Model
    $$\hat{y} = \theta_0 + \theta_1 x$$
    * Multi-dimensional Linear Model
    $$\hat{y} = \vec{\theta}\cdot\vec{x}$$
    $$\hat{\theta} = (X^T X)^{-1} X^T\vec{y}$$
    * Errors
      * Training and Testing Datasets
      * Mean Absolute Error
    $$MAE = \frac{1}{n}\sum_i |y_i-\hat{y}|$$
      * Mean Square Error
    $$MSE = \frac{1}{n}\sum_i (y_i-\hat{y})^2$$
      * Root Mean Square Error
    $$RMSE = \sqrt{MSE}$$