#  Iris Dataset Classification using KNN and Decision Tree

This project demonstrates classification on the classic **Iris flower dataset** using two supervised learning models:
- **K-Nearest Neighbors (KNN)**
- **Decision Tree Classifier**

Both models are evaluated based on accuracy and confusion matrices, along with rich visualizations using Seaborn to understand the relationships among features.

---

##  Dataset Overview

The Iris dataset consists of **150 samples** from three different species of iris flowers (`Setosa`, `Versicolor`, `Virginica`), each described by four features:
- Sepal length
- Sepal width
- Petal length
- Petal width

The goal is to **predict the species** based on these features.

---

##  Data Preparation

- The dataset was loaded using `sklearn.datasets`.
- The data was converted into a **Pandas DataFrame** with proper column names for easier manipulation and visualization.
- The target column (species) was added to the DataFrame.

---

##  Feature Scaling

- **StandardScaler** was applied to the feature set to **standardize** them (mean = 0, variance = 1).
- This step is crucial for distance-based models like **KNN**, as it ensures fair distance calculations.

---

##  Data Visualization

###  Correlation Heatmap
- A heatmap was generated using **Seaborn** to visualize correlation coefficients between features.
- It helps identify which features are most related and potentially most important for classification.

###  Pairwise Plot
- A **pairplot** was created to observe feature distributions and how well the classes separate visually in different feature combinations.
- Colors were assigned based on the target species using the `hue` parameter.

---

##  Model Building and Evaluation

The dataset was split into training and testing sets using an 80/20 split with a fixed random seed (`random_state=42`) to ensure reproducibility.

###  Model 1: K-Nearest Neighbors (KNN)
- Trained on the **scaled feature set**.
- Achieved **100% accuracy** on the test set.
- Evaluated using a **confusion matrix** and **classification report**.

###  Model 2: Decision Tree Classifier
- Trained on the **original (unscaled) feature set**, since decision trees do not require feature scaling.
- Achieved **96% accuracy** on the test set.
- Evaluated using a **confusion matrix** and **classification report**.

---

##  Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

