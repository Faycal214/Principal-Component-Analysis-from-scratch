# Project Report: Principal Component Analysis (PCA)

## 1. Introduction
This project explores the application of **Principal Component Analysis (PCA)** on the Iris dataset, a classic dataset in machine learning. The primary objective is to reduce the dimensionality of the data while preserving its essential structure, thereby facilitating interpretation and visualization.

The analysis is based on standard Python libraries, including **NumPy**, **Pandas**, **Matplotlib**, and **Scikit-learn**. A comparison is made between a **custom implementation of PCA** and the PCA provided by Scikit-learn. This report details the steps followed, the results obtained, and the conclusions drawn.

---

## 2. Methodology

### a) Data Loading
The Iris dataset was loaded using the `load_iris` function from Scikit-learn. It consists of 150 samples belonging to three different classes: **Setosa**, **Versicolor**, and **Virginica**. The features include:
- Sepal length,
- Sepal width,
- Petal length,
- Petal width.

The data was converted into a Pandas DataFrame for easier manipulation. Features (e.g., petal width, sepal length) were stored in the variable `X`, while the sample classes were stored in `y`.

### b) Applying PCA

#### **1. Data Preprocessing**
Before applying PCA, the data was **centered** (mean = 0) and **scaled** (variance = 1) to prevent any single feature from dominating due to its scale.

#### **2. Custom PCA Model**
The custom implementation of PCA involved the following steps:
1. Calculating the **covariance matrix** to capture linear relationships between the features.
2. Extracting **eigenvalues** and **eigenvectors** to determine the primary directions of variation.
3. Projecting the data into the space defined by the principal components.

#### **3. Scikit-learn PCA**
PCA was also performed using the `PCA` class from Scikit-learn, which automates these calculations and allows for validating the consistency of results.

### c) Visualization
The transformed data was projected onto the first two principal components, and the following visualizations were created:
1. **2D Scatter Plot**: Samples were colored by their classes to analyze separability.
2. **Explained Variance Plot**: A graph showing the proportion of variance captured by each principal component.
3. **3D Visualization**: Data was represented in a three-dimensional space for better interpretation.

---

## 3. Results and Analysis

### a) Explained Variance
The analysis shows that the first two principal components explain approximately **95%** of the total variance in the data. This indicates that these two components are sufficient to represent the data while minimizing information loss.

### b) Data Visualization
1. **2D Scatter Plot**: The Setosa, Versicolor, and Virginica classes are well-separated along the first two components, with Setosa being particularly distinguishable.
2. **3D Visualization**: This representation reveals additional patterns, although the third component contributes minimal new information.

### c) Validation
The comparison between the custom implementation and the Scikit-learn PCA model showed identical results. This validates the methodology and demonstrates a strong understanding of the mathematical concepts behind PCA.

---

## 4. Conclusion
This project demonstrates the utility of PCA as a tool for exploratory data analysis and dimensionality reduction. The results highlight the relationships between the features and enable effective visualization of the data in a reduced-dimensional space.

Validation using a predefined model reinforces the credibility of the results, while the custom implementation showcases mastery of the mathematical and practical aspects of PCA. This experience could be extended to other datasets or problems where dimensionality reduction is essential.
