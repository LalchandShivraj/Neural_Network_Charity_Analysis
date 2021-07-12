# Neural_Network_Charity_Analysis

Alphabet Soup’s business team has given Beks a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization.

Using machine learning and neural networks, the task at hand is to use the features in the dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

### Planned Steps:

1.	Use Pandas and the Scikit-Learn’s StandardScaler() to Preprocessing Data for a Neural Network Model.
2.	Design a neural network to create a binary classification model that can do the required predictions. Then, Compile, Train, and Evaluate the Model.
3.	Use TensorFlow to Optimize the Model.

# Results
The charity_data.csv was imported, some columns dropped, some columns binned and then the target and features selected and set into dfs. The model was then compiled, trained and evaluated. This did not achieve the > 75% accuracy be sought.
So, three attempts were made to optimize the model.
![Del_1_and_2_performance](https://user-images.githubusercontent.com/78666055/125216196-681d1500-e28b-11eb-9eb3-6cb9c43aeb96.png)


### Optimization:

#### First Attempt:
.	Dropped EIN, NAME and USE_CASE columns.
.	Binned: APPLICATION_TYPE and CLASSIFICATION
.	Features: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
.	Target: IS_SUCCESSFUL
.	2 Hidden Layers: 80, 30 using relu activation
.	Output Layer: Sigmoid activation
.	Accuracy: 71% (Performance not achieved)
![First_Attempt](https://user-images.githubusercontent.com/78666055/125216201-6e12f600-e28b-11eb-85f9-75a46d81acd8.png)


#### Second Attempt:
.	Dropped EIN and USE_CASE columns.
.	Binned: APPLICATION_TYPE, CLASSIFICATION and NAME
.	Features: NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS
.	Target: IS_SUCCESSFUL
.	2 Hidden Layers: 80, 30 using relu activation
.	Output Layer: Sigmoid activation
.	NAME was added back and binned.
.	Accuracy: 77% (Performance achieved)*******
![Second_Attempt](https://user-images.githubusercontent.com/78666055/125216207-73704080-e28b-11eb-992d-604206f124dd.png)


#### Third Attempt:
.	Dropped EIN, NAME and USE_CASE columns.
.	Binned: APPLICATION_TYPE and CLASSIFICATION
.	Features: NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS
.	Target: IS_SUCCESSFUL
.	3 Hidden Layers: 100, 80, 30 using relu and sigmoid actv.
.	Output Layer: Sigmoid activation
.	Accuracy: 77% (Performance not achieved)
![Third_Attempt](https://user-images.githubusercontent.com/78666055/125216228-7b2fe500-e28b-11eb-8c6a-2a43d5ce5e3a.png)


# Summary

The second attempt achieved the required accuracy of over 75%. 
Even though the third attempt did not produce a favourable result, I feel modifying the neurons and the activation type of the hidden layers, an even better result than the second attempt may be obtained.
