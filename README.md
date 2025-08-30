🧠 Lumbar Fracture Risk Prediction with Multi-Task Learning

This project leverages deep learning to estimate T-scores and classify lumbar fracture risk from vertebral microarchitecture data. The workflow includes data preprocessing and multi-task model training.

📁 Notebooks
Data_Preprocessing.ipynb

Purpose: Prepare and clean the dataset for model training.

Key operations:

Load data extracted from lumbar vertebrae images (each vertebra divided into 9 anatomical zones).

Filter & clean features:

Remove outliers

Select relevant metrics (e.g., BV/TV, Tb.Th mean, BMD)

Normalize numerical features

Encode categorical variables (e.g., vertebra level, zone)

Save the preprocessed dataset for training

Output: Clean dataset with input features (X) and targets (T-score, risk class).

MultiTask_Model_Training.ipynb

Purpose: Train a neural network for simultaneous regression (T-score) and classification (fracture risk).

Workflow:

Load preprocessed dataset

Split into training and test sets

Define multi-task neural network in Keras:

Shared hidden layers

Regression output for T-score

Classification output for risk category

Compile model with two losses:

MSE for regression

Categorical cross-entropy for classification

Train and monitor both outputs

Evaluate performance:

MAE/RMSE for T-score

Accuracy, precision, recall for fracture risk

✅ Requirements

Install required packages:

pip install numpy pandas scikit-learn tensorflow matplotlib

📌 How to Use

Run Data_Preprocessing.ipynb to create the cleaned dataset.

Run MultiTask_Model_Training.ipynb to train and evaluate the model.
