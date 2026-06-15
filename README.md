# Diabetes Prediction

A Jupyter Notebook that explores a binary classification workflow for predicting diabetes outcomes from diagnostic measurements.

## Approach

The notebook:

- loads and inspects the diabetes dataset
- separates input features from the outcome
- standardizes numerical features
- creates stratified training and test sets
- trains a linear Support Vector Machine
- evaluates training and test accuracy
- demonstrates a prediction for a new input

## Dataset

The model expects the commonly used Pima Indians Diabetes dataset with these fields:

`Pregnancies` `Glucose` `BloodPressure` `SkinThickness` `Insulin` `BMI` `DiabetesPedigreeFunction` `Age` `Outcome`

The dataset is not included in this repository. Update the CSV path in the notebook before running it.

## Run

```bash
pip install numpy pandas scikit-learn jupyter
jupyter notebook PROJECT2Diabetes.ipynb
```

Run the notebook cells in order.

## Disclaimer

This is an educational machine learning project and must not be used for medical diagnosis or treatment decisions.
