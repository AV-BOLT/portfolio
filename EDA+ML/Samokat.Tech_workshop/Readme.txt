The goal of this work is to determine whether there is a match between two products. We have data on products available in the market and products offered by merchants. Therefore, our task involves binary classification, where 1 indicates a match, and 0 signifies the absence of a match. Metrics should be F1 score, as set by the hosts of the workshop.

This workshop is run as a contest on the Kaggle platform, leading to several particularities:

Handling tails poses a challenge because the test data must be processed similarly to the train data. However, in the case of dropping tails, they should be dropped in the test data as well. On Kaggle, the test data must contain the same number of rows as in a given.
Another consideration is the size of the dataset. It may be challenging to scale the data, and models that rely on scaled data, such as SVM and neural networks, might be prohibited.
I'll start with tree-based models like CatBoost, Light GBM, and those using gradient boosting, considering the discussed factors in machine learning. I will perform hyperparameter tuning using the Optuna framework, taking into account the dataset size and other considerations.

If the outcome is unsatisfactory, I will turn to pretrained neural networks like Siamese. My observation is fitting models in batches is straightforward and won't lead to memory limit exceedances. However, scaling could be a real challenge with large datasets, especially considering I rely on open sources like Google Colab and Kaggle.

I won't use cross-validation; instead, I'll split the data into train and validation sets.
