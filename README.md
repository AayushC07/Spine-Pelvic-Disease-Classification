# Vertebral Column Classification using KNN - DSCI 552 Project

This project applies various K-Nearest Neighbors (KNN) classification techniques to the **Vertebral Column Data Set** from the UCI Machine Learning Repository. The objective is to perform binary classification (Normal = 0, Abnormal = 1) based on six biomechanical features of the human spine.

## 📂 Dataset
- **Source**: [Vertebral Column Data Set](https://archive.ics.uci.edu/ml/datasets/Vertebral+Column)
- **Attributes**:
  - Pelvic incidence
  - Pelvic tilt
  - Lumbar lordosis angle
  - Sacral slope
  - Pelvic radius
  - Grade of spondylolisthesis

## 🧪 Project Tasks

### 1. Data Preprocessing & EDA
- Converted categorical class labels to binary values: Normal (0) and Abnormal (1).
- Plotted:
  - **Scatter plots** of all feature pairs colored by class.
  - **Box plots** of individual features colored by class.
- Created a training set using the first 70 instances of class 0 and first 140 instances of class 1, with the remainder used for testing.

### 2. KNN Classification
- Implemented standard KNN using the Euclidean distance.
- Evaluated performance across a range of `k` values from 208 down to 1.
- Computed performance metrics:
  - Confusion Matrix
  - True Positive Rate (TPR)
  - True Negative Rate (TNR)
  - Precision
  - F1-Score
- Identified the best value of `k` based on minimum test error.

### 3. Learning Curve
- Plotted **test error vs. training set size** using the best-performing `k` for each size.
- Training sizes ranged from 10 to 210 (in steps of 10), with proportional class representation.

### 4. Distance Metric Variants
Explored alternative distance metrics in KNN:
- **Minkowski Distance**
  - Manhattan Distance (p = 1)
  - Chebyshev Distance (p → ∞)
  - Varying `log10(p)` from 0.1 to 1
- **Mahalanobis Distance**

Test error results for the best `k` were summarized in a comparison table.

### 5. Weighted KNN
- Replaced majority voting with **distance-weighted voting**.
- Applied with Euclidean, Manhattan, and Chebyshev distances.
- Reported best-performing test errors using weighted KNN.

### 6. Final Results
- Identified the **lowest training error rate** achieved.
- Compared different techniques for accuracy and robustness.

## 📊 Key Concepts Used
- K-Nearest Neighbors
- Distance Metrics (Euclidean, Manhattan, Chebyshev, Minkowski, Mahalanobis)
- Weighted Voting
- Learning Curves
- Evaluation Metrics (Confusion Matrix, Precision, F1-score, etc.)

## 💻 Technologies Used
- Python
- NumPy, Pandas
- scikit-learn
- Matplotlib, Seaborn

## 📈 Visualizations
- Feature distributions by class
- Train/Test error vs. `k`
- Learning curves across dataset sizes
- Error comparison across different distance metrics and voting methods

## 📁 Structure
project-folder/
│
├── data/ # Contains the dataset (optional if downloadable)
├── notebooks/ # Jupyter notebooks with code and analysis
├── plots/ # Generated plots for EDA and results
├── knn_classification.py # Core KNN implementations and evaluation scripts
└── README.md # Project description (this file)

📌 Acknowledgment
This project was completed as part of DSCI 552 (Machine Learning for Data Science) course at the University of Southern California, instructed by Dr. Mohammad Reza Rajati.
