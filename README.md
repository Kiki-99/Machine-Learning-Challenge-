![Planet Picture](/Images/exoplanets.jpg)

# Machine-Learning- Exoplanet Exploration #


## Background ##

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.  To help process this data, you will create machine learning models capable of classifying candidate exoplanets from the raw dataset.


## Data Source ##

[Exoplanet Search Results](https://www.kaggle.com/nasa/kepler-exoplanet-search-results) This dataset contains over 10,000 exoplanet candidates examined by the Keplar Space Observatory.  This orbital telescope's primary goal is to search for exoplanets in star systems other than our own with the ultimate goal being to indentify habitable planets other than our own


## Machine Learning Model Process ##

Models Selected -->  Logistic Regression |  Random Forest | Support Vector Classification

- **Preprocess the Raw Data**
  - Preprocessed the dataset prior to fitting the model.
  
  - Performed feature selection and removed unnecessary features.
  
      - Apply the `RFE` method to identify the importance of each feature.
      
      - Selected only the features that support the outcome.
      
  - Used `MinMaxScaler` to scale the numerical data.
  
  - Separated the data into training and testing data.

- **Tune Model Parameters**

  - Use [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html) to tune model parameters.
  
  - Tuned the model
  
- **Compare Models created**

  - Using model accuracy and resources used for choosing the best model

## Model Selection ##

After running Fit/Test/Training on the data with three seperate models, the model that would be the best estimator for prediction of candidate exoplanets is Linear SVC (Support Vector Classification):

  - The model will predict categorical output (y).

  - y is a labeled data point.

  - There are less than 100K samples in the dataset.

After training and fitting a model with selective features, applying `GridSearchCV` to tune the best model with different parameters. The result shows that the best parameter is **'C': 1000, 'gamma': 1, 'kernel': 'linear' with 88.32% accuracy.**


![SVM Selection](/Images/svm_parameter_range.JPG)


### Outputs ###


![Outputs](/Images/best_parameter.JPG)


### Model Summary ###


![Model Summary](/Images/model_summary.JPG)


## Conclusion ##


**Logistic Regression Accuracy** | **Random Forest Accuracy** | **Support Vector Classification**
--------------------- | --------------------- | ---------------------
![LR Accuracy](/Images/lr_accuracy.JPG)|![RF Accuracy](/Images/rf_accuracy.JPG)|![SVC Accuracy](/Images/svm_accuracy.JPG)


In conclusion, the model that will be the best estimator for predicting exoplanet canidates is the Linear Support Vector Classification.  The chart above shows that even though the Random Forest model's accuracy is higher than the SVC model's accuracy, the training model duration was about 30 mins for Random Forest and 5 minutes for SVC with less than 100K samples. Therefore, if we take into consideration the time and resources it takes for model creation, the SVC model tends to perform well within a limited budget and time.
