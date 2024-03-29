# Predicting Handwritten Digit
To predict handwritten digit (0~9), I built a Multiclass Logistic Regression in R using Kaggle dataset [mnist_test](https://www.kaggle.com/oddrationale/mnist-in-csv), which is an image pixel dataset.
## Inrtroduction
Generalized Linear Model (GLM) is a flexible generalization of ordinary linear regression. To be more specific, GLM allows for response variables that have error distribution models other than a normal distribution. In this project, I applied one type of GLM, Logistic Regression Model, to predict handwritten digits. Since it is a multiclass classification problem, I utilized Multiclass Logistic Regression, which is also called Multinomial Logistic Regression or Softmax Regression.
## Exploratory Data Analysis
   - Plot images
   - Plot digit labels distribution
## Data Preprocessing
   - Examine missing value
   - Split into training (0.8) and test (0.2)
## Modeling: Supervised Learning
Multiclass logistic regression
   - I used For loop to build 10 logistic regression models, one per digit.
   - I used the Softmax function to transform unrelated probabilities into a probability distribution over 10 digits.
   - The predicted digit will be the one associated with the maximum probability.
## Multiclass Classification Model Evaluation
   - Overall accuracy
   - True Positive Rate (sensitivity/ recall) of each digit
## Conclusion
To sum up, I trained 10 models, one per digit, and used the Softmax function to turn unrelated probabilities into related probabilities. Finally, with predicted results, I built a confusion matrix and calculated the overall accuracy. 

Digit|0|1|2|3|4|5|6|7|8|9
-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----
**Sensitivity (TPR)**|0.8245|0.9124|0.7540|0.7423|0.7286|0.6378|0.7347|0.8350|0.6585|0.7220

From the model results, I found that digit 1 has the highest TPR, above 90%, and digits 0 and 7 also have high TPR, above 80%. However, digits 5 and 8 have lower TPR, only around 65%. That is to say, the model can highly correctly recognize handwritten digits of 1, 0, and 7, but can not recognize handwritten digits of 5 and 8 very well.
