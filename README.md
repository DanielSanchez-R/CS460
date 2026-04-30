# CS460
Capstone Project

# Swarm Behaviour Machine Learning Project

## Project Overview

This project uses the **Swarm Behaviour** dataset from the UCI Machine Learning Repository to classify different types of swarm movement behavior using supervised machine learning models.

The dataset contains three binary classification datasets.

Each dataset is used to predict whether a swarm is showing a specific behavior or not. The class labels are binary, where `1` represents the presence of the behavior and `0` represents the absence of the behavior. For example, in the Flocking dataset, `1` means flocking and `0` means not flocking.

According to the UCI Machine Learning Repository, this is a multivariate classification dataset with real-valued features. It contains 24,017 instances and 2,400 features. The dataset includes three behavior categories: flocking/not flocking, aligned/not aligned, and grouped/not grouped. :contentReference[oaicite:0]{index=0}

## Dataset Variable Information

The Swarm Behaviour dataset describes the movement and interaction patterns of simulated swarm agents, also called boids.

The variables include position, velocity, alignment, separation, cohesion, and neighborhood-count information for the boids. According to the UCI dataset description, the attributes include:

- `x`, `y`: the X and Y position of each boid
- `xVel`, `yVel`: the X and Y velocity vector values
- `xA`, `yA`: the alignment vector values
- `xS`, `yS`: the separation vector values
- `xC`, `yC`: the cohesion vector values
- `nAC`: the number of boids within the alignment/cohesion radius
- `nS`: the number of boids within the separation radius
- `Class`: the binary target label

These attributes are repeated for each boid in the dataset. The class label is binary, where `1` represents flocking, grouped, or aligned behavior, depending on the dataset, and `0` represents not flocking, not grouped, or not aligned. :contentReference[oaicite:1]{index=1}

## Files Used

The main dataset files are:

- `Aligned.csv`
- `Flocking.csv`
- `Grouped.csv`

These files can be downloaded from the UCI Machine Learning Repository:

https://archive.ics.uci.edu/dataset/524/swarm+behaviour

## Notebook Workflow

The main notebook follows this workflow:

Objective
1. Import Libraries
2. Load the Datasets
3. Data Cleaning and Initial Inspection
4. Initial EDA on Whole Dataset
5. Feature/Target Separation and Train-Test Split
6. Preliminary Training-Data Diagnostics
7. Train/Test Split Verification and PCA Exploration
8. Model Selection Logic
9. Hyperparameter Tuning Setup
10. Model Training Runs
11. Consolidated Model Results
12. Final Best Model Selection
13. Error Analysis
14. Confusion Matrices
15. Metrics
16. Prediction Examples
17. Conclusion

## Running the Notebook

This project was developed in **Google Colab** using Python:

The notebook uses the following libraries and modules:

- `os`
- `ast`
- `random`
- `time`
- `pickle`
- `re`
- `warnings`
- `numpy`
- `pandas`
- `matplotlib.pyplot`
- `seaborn`
- `google.colab.files`
- `mpl_toolkits.mplot3d.Axes3D`
- `xgboost.XGBClassifier`

The notebook also uses the following `scikit-learn` tools:

- `clone`
- `train_test_split`
- `GridSearchCV`
- `RandomizedSearchCV`
- `StratifiedKFold`
- `StandardScaler`
- `PCA`
- `Pipeline`
- `LogisticRegression`
- `RidgeClassifier`
- `DecisionTreeClassifier`
- `LinearSVC`
- `RandomForestClassifier`
- `accuracy_score`
- `precision_score`
- `recall_score`
- `f1_score`
- `roc_auc_score`
- `confusion_matrix`
- `ConfusionMatrixDisplay`
- `roc_curve`
- `auc`

The File already has all complete outputs.

However, if you wanted to run the worklow again simply:

To run the notebook from the beginning, upload the three dataset files into Google Colab session storage and execute the notebook cells in order.

## Important Note About Section 10: Model Training Runs

The model training section can take a long time to run in Google Colab because the datasets are large and high-dimensional.

If you do not want to rerun the full **Model Training Runs** section, you can use the saved partial result files included in the "extra" folder within the GitHub repository.

These files are located in the:PartialFiles folder. Simply upload them into Google Colab session storage.
