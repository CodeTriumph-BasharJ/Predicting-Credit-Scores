This project aims to predict the credit score category (Good, Poor, Standard) for 100,000 individuals based on factors such as monthly salary, investments, debit amount, debt payments, credit utilization ratio, payment behavior, number of credit cards, age, and occupation. The solution involves three modified versions of a standard genetic algorithm, described as follows:

1. The fitness function assigns random weights to each attribute and selects the top 80% of examples with the lowest sum of weights to enhance the algorithm's learning process. The maximum achieved accuracy was around 55%.

2. This version of the fitness function also randomizes weights for each attribute. After each iteration, the weights are adjusted based on the error margin between the current and previous sets. If the current weights result in a lower error margin, they are refined further by comparing and adjusting the weights based on their indices. 80% of the best examples with the highest scores are selected in each iteration of the algorithm. The maximum achieved accuracy was around 75%.

3. The third version uses a Decision Tree Classifier, where 80% of the data is used for training in each iteration. The fitness score is determined by the error margin between predicted and actual credit scores. The top 100% of examples with the highest scores are selected to optimize the learning process in each iteration. This version achieved a maximum accuracy of around 99%.

For all algorithm versions, testing was conducted on 20% of the original dataset (20,000 individuals). The efficiency of the algorithms was assessed by averaging the scores for each credit score category and then using the best weights or Decision Tree model to predict and compare the testing data's credit scores. The highest efficiency was achieved when the similarity percentage was set to 70% for the first two models and 60% for the third.

More information about the data: https://www.kaggle.com/datasets/parisrohan/credit-score-classification
