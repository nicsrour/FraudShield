# FraudShield
## Machine Learning Model for Credit Card Fraud Detection
This project aims to develop a machine learning model capable of predicting credit card frauds using historical credit card transaction data that includes information such as date, time, amount, location, transaction type, cardholder information, and others.

To accomplish this, a classification algorithm such as Random Forest or KNN will be applied to train the model with the historical data. During training, cross-validation techniques and hyperparameter tuning will be used to ensure that the model is robust and has good performance.

Finally, the model will be evaluated using a set of unseen credit card transaction data, and its predictions will be compared with actual transactions. Evaluation metrics such as precision, recall, and F1-score will be used to assess the model's performance.

The project will be implemented in Python, using popular machine learning libraries such as Scikit-learn and Pandas to facilitate data analysis and model implementation.

Several machine learning models have been developed for detecting credit card fraud, and in this banking scenario, recall is the main metric to be analyzed because banks want to identify all fraud cases, avoiding customer compensation.

Among the models, there is an unbalanced Random Forest model, which obtained a precision of 0.79 and recall of 0.66. There is also a model developed with the under-sampling (Near miss) technique, which obtained a precision of 0.11 and recall of 0.84. Finally, the model developed with over-sampling obtained a precision of 0.71 and recall of 0.73.

Each model presents different results, and the bank manager should carefully analyze them before deciding which model is most appropriate for their needs. If the bank wants to identify the highest possible number of frauds, even if that results in identifying legitimate transactions as fraudulent, then the model with higher recall (Near miss) may be the best choice.

On the other hand, if the bank wants to minimize the number of false positives and ensure that most identified fraudulent transactions are indeed fraudulent, then the most suitable model would be the over-sampling model.

Regardless of the chosen model, it is important to note that no model is 100% accurate. Therefore, the best approach may be to use the model as a tool to apply a second layer of identification to transactions that are judged as fraudulent by the model. Thus, the bank can ensure that most suspicious transactions are identified and evaluated before being completed.

Simulation with Near Miss model (recall 0.84)

Knowing that the total loss value of the bank is 5121413.29, identifying and preventing 84% of these transactions would be equivalent to saving 4301987.16.