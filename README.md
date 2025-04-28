📂 Project Structure
Lens Simulation: Defines a Heliar lens model and traces randomly generated rays through it.

Data Generation: Generates labeled datasets indicating whether rays successfully reach the image plane.

Data Analysis: Explores the data with statistical summaries and correlation heatmaps.

Modeling:

Applies SMOTE to handle class imbalance.

Scales features with StandardScaler.

Trains Random Forest and Logistic Regression models.

Evaluation: Evaluates models using accuracy, confusion matrices, ROC curves, and Precision-Recall curves.

🛠️ Libraries Used
optiland - Optical simulation and ray tracing

numpy

pandas

matplotlib

seaborn

scikit-learn

imbalanced-learn (SMOTE for oversampling)

🚀 How to Run
Install required packages:

bash
Copy
Edit
pip install optiland scikit-learn imbalanced-learn matplotlib seaborn pandas
Run Ray_path.ipynb notebook step-by-step.

Outputs will include:

Sample data

Correlation heatmap

Classification reports

Confusion matrices

ROC and Precision-Recall curves

📊 Results
Random Forest generally achieves higher accuracy and ROC AUC than Logistic Regression.

SMOTE helps balance the dataset and improves classification performance.

🔮 Future Enhancements
Implement more advanced lens designs.

Try other classifiers (e.g., XGBoost, SVM).

Perform hyperparameter tuning using GridSearchCV or RandomizedSearchCV.

Extend to multi-class classification for more detailed ray outcomes.
