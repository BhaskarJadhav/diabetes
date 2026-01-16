# Diabetes Prediction Model

This project implements a machine learning model to predict the likelihood of diabetes based on diagnostic measurements. The model uses a Support Vector Machine (SVM) classifier.

## Dataset

The dataset used for this project is `diabetes.csv`. It contains various health-related features and an `Outcome` column indicating whether a person has diabetes (1) or not (0).

**Features:**
*   `Pregnancies`: Number of times pregnant
*   `Glucose`: Plasma glucose concentration a 2 hours in an oral glucose tolerance test
*   `BloodPressure`: Diastolic blood pressure (mm Hg)
*   `SkinThickness`: Triceps skin fold thickness (mm)
*   `Insulin`: 2-Hour serum insulin (mu U/ml)
*   `BMI`: Body mass index (weight in kg/(height in m)^2)
*   `DiabetesPedigreeFunction`: Diabetes pedigree function
*   `Age`: Age (years)

**Target Variable:**
*   `Outcome`: 0 for non-diabetic, 1 for diabetic.
*   ## Methodology

The project follows these steps:

1.  **Data Loading**: The `diabetes.csv` dataset is loaded into a pandas DataFrame.
2.  **Data Preprocessing**: Features (X) and target (y) are separated. The features are then standardized using `StandardScaler` to bring them to a common scale, which is crucial for SVM performance.
3.  **Train-Test Split**: The dataset is split into training and testing sets (80% training, 20% testing) to evaluate the model's performance on unseen data. Stratified sampling is used to maintain the proportion of diabetic/non-diabetic outcomes in both sets.
4.  **Model Training**: A Support Vector Machine (SVM) classifier with a linear kernel is trained on the standardized training data.
5.  **Model Evaluation**: The model's accuracy is evaluated on both the training and testing datasets.

  ## Results

After training and evaluation, the model achieved the following accuracy scores:

*   **Training Data Accuracy**: 76.55%
*   **Test Data Accuracy**: 82.47%

These results indicate that the model performs well and generalizes reasonably to new, unseen data.


## How to Make a Prediction

To use the trained model for prediction, you need to provide a new input data point with the same features as the training data. This input data must also be standardized using the same `StandardScaler` fitted during the training phase.

### Example Input Data:

`input_data = (4, 110, 92, 0, 0, 37.6, 0.191, 30)`

This input will be transformed and then fed to the `classifier.predict()` method. The output will be `[0]` for non-diabetic or `[1]` for diabetic.
