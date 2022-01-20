# Permutation Feature Importance
Permutation feature importance is a model inspection technique that can be used for any fitted estimator when the data is tabular. This is especially useful for non-linear or opaque estimators. The permutation feature importance is defined to be the decrease in a model score when a single feature value is randomly shuffled. This procedure breaks the relationship between the feature and the target, thus the drop in the model score is indicative of how much the model depends on the feature. This technique benefits from being model agnostic and can be calculated many times with different permutations of the feature
## Realization
Write the function that will read the data and the number of important features and return the false positives with original fratures, feature importance score_orig-score_perm, and fp with the given number of important features
1. Read the credit data set (train and test)
2. Predict the test set with Decision Tree Classifier and return the original model score and the number of false positives
3. Iterate through all the features np.random.permutation and calculate the feature importance as score_orig - score_temp
4. Create dictinary with FP without permutation, tuple of important features in an ascending order, and FP using n most 
important features
