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
  - Tune model
  
- **Compare Models created**
  - Using model accuracy and resources used for choosing the best model

## Model Selection ##


### Outputs ###


### Model Summary ###


## Conclusion ##


As the graph presented above, it shows that the Random Forest model accuracy is higher than SVC model accuracy. However, training model duration was about an hour for Random Forest and 5 minutes for SVC with less than 100K samples. Therefore, if the model creation takes time and resources used into consideration, the SVC model tend to perform well within a limited budget and time.
