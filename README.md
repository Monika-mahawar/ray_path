 
This project demonstrates the simulation of ray paths through a Heliar lens system and classification of ray tracing success using machine learning models.

The project involves:

Optical simulation using the optiland package.

Data generation for ray paths.

Exploratory Data Analysis (EDA) on the generated dataset.

Data preprocessing including balancing with SMOTE and scaling.

Training and evaluating machine learning models (Random Forest and Logistic Regression) to predict whether a ray successfully reaches the image plane.

Project Structure
Lens Simulation:

A custom HeliarLens class is created based on optical surface data.

Random rays are generated and traced through the lens.

Data Analysis:

Features include ray positions and directions.

Success/failure of ray reaching the image plane is labeled.

Correlation matrix is visualized using Seaborn.

Machine Learning Pipeline:

Data is split into training and testing sets.

Data imbalance is addressed using SMOTE.

Features are standardized using StandardScaler.

Models used:

Random Forest Classifier

Logistic Regression

Evaluation Metrics:

Accuracy

Classification Report

Confusion Matrix

ROC-AUC Score

ROC Curve

Precision-Recall Curve

Installation
First, make sure the required packages are installed:

bash
Copy
Edit
pip install optiland
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn
Running the Code
Import Libraries
Import all necessary libraries including optiland, numpy, pandas, scikit-learn, etc.

Define Lens
Create a HeliarLens class using the optic.Optic base class from optiland, defining each optical surface.

Generate Random Rays
Function get_random_rays(num_rays, seed) generates random rays in object space with random direction vectors.

Trace Rays
Function trace_random_rays(num_rays) traces these random rays through the lens and records if they successfully reach the image plane.

Exploratory Data Analysis (EDA)

View class distribution.

Check feature statistics using describe().

Plot correlation matrix.

Preprocessing

Split the dataset into training and test sets (80/20).

Use SMOTE to balance classes.

Scale features using StandardScaler.

Model Training and Evaluation

Train a Random Forest and Logistic Regression model.

Compare performances based on accuracy, ROC-AUC, and classification metrics.

Plot Results

Confusion matrices

ROC curves

Precision-recall curves

Key Functions

Function	Purpose
HeliarLens	Defines the multi-element Heliar lens.
get_random_rays(num_rays, seed)	Generates random initial rays.
trace_random_rays(num_rays)	Traces rays through the lens and generates a labeled dataset.
Example Outputs
Correlation Matrix
A heatmap showing correlations between position and direction vectors.

Confusion Matrices
Performance comparison of Random Forest vs Logistic Regression on test data.

ROC and Precision-Recall Curves
Visual comparison of model performances in distinguishing successful rays.

Results Summary

Model	Accuracy	ROC-AUC
Random Forest	~ High	High
Logistic Regression	Slightly Lower	Slightly Lower
Random Forest slightly outperforms Logistic Regression across all metrics.

Notes
SMOTE was critical to handle class imbalance (more rays fail than succeed).

Scaling improves Logistic Regression performance (Random Forest is less sensitive).

Randomness in ray generation is controlled by setting a seed to ensure reproducibility.

Future Improvements
Try other classifiers like XGBoost, SVM.

Tune hyperparameters (RandomizedSearchCV / GridSearchCV).

Experiment with deeper lens models or distorted input rays.

Deploy as a web app to simulate rays live!
