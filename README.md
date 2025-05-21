This project analyzes and classifies events from the Magic Gamma Telescope dataset to distinguish between gamma rays and hadrons using various machine learning models.

## Dataset

The dataset used is the Magic Gamma Telescope Data, sourced from "magic04.data". The features are measurements from the telescope, and the target variable indicates whether the event was a gamma ray or a hadron.

The dataset includes the following columns:
- fLenght
- fwidth
- fSize
- fConc
- fConc1
- fAsym
- fM3Long
- fM3Trans
- fAlpha
- fDist
- class (target: 'g' for gamma ray, others for hadron)

## Project Structure

The code performs the following steps:

1.  **Data Loading and Preprocessing:** Loads the data from the CSV file, assigns column names, and converts the target variable into a binary numerical format (1 for gamma, 0 for hadron).
2.  **Exploratory Data Analysis:** Visualizes the distribution of each feature for both classes using histograms.
3.  **Data Splitting:** Splits the dataset into training, validation, and testing sets (60% train, 20% validation, 20% test).
4.  **Scaling and Oversampling:**
    *   Scales the features using `StandardScaler`.
    *   Applies Random Oversampling to the training data to address potential class imbalance.
5.  **Model Training and Evaluation:** Trains and evaluates the following classification models:
    *   k-Nearest Neighbors (kNN)
    *   Gaussian Naive Bayes
    *   Logistic Regression
    *   Support Vector Machine (SVC)
    For each model, a classification report is printed to show performance metrics (precision, recall, f1-score, support).
