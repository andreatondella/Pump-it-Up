# Pump it Up: Data Mining the Water Table

Using data from Taarifa and the Tanzanian Ministry of Water, can you predict which pumps are functional, which need some repairs, and which don't work at all? This is an intermediate-level practice competition. Predict one of these three classes based on a number of variables about what kind of pump is operating, when it was installed, and how it is managed. A smart understanding of which waterpoints will fail can improve maintenance operations and ensure that clean, potable water is available to communities across Tanzania.

## Notebook
This notebook is structured in eight main sections:
* **Data Cleaning:** where all the variables are inspected and the necessary steps are taken in order to remove missing values, correct errors, remove redundant features and apply the necessary transformations.
* **Feature Engineering:** where some new features are created from the combination of other existing features.
* **Exploration:** where the relation between some interesting variables status_group is analyzed.
* **PCA and LDA:** where some dimensionality reduction techniques are tested in an attempt to visualize the dataset in 2 and 3 dimensions.
* **Baseline Models:** where the following models are fitted to the data to get a baseline score: Random Forest, XGBoost, KNN, LDA and KNN after LDA.
* **Hyperparameter tuning:** where the parameters of Random Rorest and XGBoost are tuned by means of iterated random searches. **Best Score Overall (0.8201)** obtained by random forest after parameter tuning.
* **Model Stacking:** where Random Forest and XGBoost after parameter tuning are stacked by means of a random forest.
* **Specialized Random Forests:** where three different Random Rorests are trained to predict a particular status_group in a "one vs the rest" fashion. The three forests are then stacked together by means of a logistic regression.
