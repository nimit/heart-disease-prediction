# Heart Disease Prediction

## Code
```Heart Disease Prediction.ipynb``` - Contains the entire code of the project with the project pipeline including all the way from data preprocessing to algorithms implemented and analysis

## Dataset
```cardio_dataset.csv``` - Comma Seperated Values(.csv) file which includes the data related to patients diagnosed/not diagnosed with coronary heart disease (CHDs)

## Libraries Used
I used the following libraries:
1. Pandas and Numpy: For data manipulation
2. Matplotlib and Seaborn: For visualization
3. Scikit-learn: For ML models, training and testing
4. Pandas-profiling - External library used for Exploratory Data Analysis

## Results
The following results were obtained after applying different supervised learning techniques, before and after using dimensionality reduction using Principal Component Analysis(PCA).

The following ML algorithms were applied:
* Logistic Regression
* K-Nearest Neighbor
* Linear Discriminant Analysis
* Naive Bayes
* Decision Tree
* Support Vector Machine

The results are tabulated below.

### Without applying PCA

| Classifier  		| Test Accuracy | Precision 	| Recall 		| F1 Score 		|
|    :----:   		|    :----:   	|     :----:    |     :----:    |     :----:    |
|KNN           		| 0.7227 		| 0.73 			| 0.72 			| 0.72 			|
|Logistic Regression| 0.7201 		| 0.72 			| 0.72 			| 0.72 			|
|Naive Bayes 		| 0.70863 		| 0.71 			| 0.71 			| 0.71 			|
|Decision Tree 		| 0.70639 		| 0.71 			| 0.71 			| 0.70 			|
|SVM 				| 0.72679 		| 0.73 			| 0.73 			| 0.73 			|
|LDA 				| 0.72143 		| 0.72 			| 0.72 			| 0.72 			|


### After applying PCA

| Classifier  		| Test Accuracy | Precision 	| Recall 		| F1 Score 		|
|    :----:   		|    :----:   	|     :----:    |     :----:    |     :----:    |
|Logistic Regression| 0.7159 		| 0.72 			| 0.72 			| 0.71 			|
|Naive Bayes 		| 0.6883 		| 0.70 			| 0.69 			| 0.68 			|
|Decision Tree 		| 0.6430 		| 0.66 			| 0.64 			| 0.63 			|
|SVM 				| 0.7196 		| 0.72 			| 0.72 			| 0.72 			|
|LDA 				| 0.7150 		| 0.72 			| 0.72 			| 0.71 			|

### ROC Curves

<img src="https://user-images.githubusercontent.com/62750523/202967813-6a67facc-3a52-43f3-ac30-bbadfd77072b.jpg" alt="roc curves w/o pca" width="500"/> <img src="https://user-images.githubusercontent.com/62750523/202967854-160426e3-bcd5-487f-bb64-16065a097f60.jpg" alt="pca roc curves" width="500"/>


## Conclusions
The best accuracy obtained was using SVM without dimensionality reduction of ```72.679%```. Changing hyperparameters(C and gamma) or using kernel tricks further lowered accuracy indicating that the default hyperparameters and linear kernel provide the best fit to the training data.
After applying PCA, the highest accuracy obtained was ```71.96%```(SVM).
