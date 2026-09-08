# IMDb KNN Classification

A beginner-friendly machine learning project that uses **K-Nearest Neighbors (KNN)** to classify IMDb movies as high-rated or not high-rated.

## Objective

The target is created from the IMDb rating:

- `1` = High Rated (`IMDB_Rating >= 8.0`)
- `0` = Not High Rated (`IMDB_Rating < 8.0`)

`IMDB_Rating` is used only to create the target and is **not** included in the input features.

## Features

The model uses:

- Released Year
- Runtime
- Genre
- Certificate
- Meta Score
- Number of Votes
- Gross Revenue

Genre and Certificate are one-hot encoded. Number of Votes and Gross Revenue are log-transformed because their values are highly skewed.

## KNN Concepts Practiced

This project was created for educational practice and covers:

- `KNeighborsClassifier`
- Choosing the value of `K`
- `weights="uniform"` vs `weights="distance"`
- Manhattan vs Euclidean distance
- `algorithm="auto"`, `"brute"`, `"kd_tree"`, and `"ball_tree"`
- Feature scaling with `StandardScaler`
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Classification Report

## Model Selection

The data is split into:

- 60% Train
- 20% Validation
- 20% Test

KNN hyperparameters are selected using **F1 score on the validation set**, while the test set is kept untouched until final evaluation.

The notebook also contains an optional decision-threshold experiment to study the Precision/Recall trade-off and potentially improve F1 for the High-Rated class.

## Project Structure

```text
IMDB_KNN_Classification/
├── data/
│   └── imdb_top_1000.csv
├── notebooks/
│   └── imdb_KNN.ipynb
├── .gitignore
├── README.md
└── requirements.txt
```

## Installation

Install the required packages:

```bash
pip install -r requirements.txt
```

Then open:

```text
notebooks/imdb_KNN.ipynb
```

and run the cells from top to bottom.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Purpose

This project was created for educational purposes to practice KNN classification and basic machine learning workflow on a real movie dataset.
