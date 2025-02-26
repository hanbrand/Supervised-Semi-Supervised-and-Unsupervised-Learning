# Supervised, Semi-Supervised, and Unsupervised Learning

## Overview

This project explores different **machine learning paradigms**—supervised, semi-supervised, and unsupervised learning—using real-world datasets. The goal is to compare the effectiveness of various approaches using **SVMs, K-Means, and Spectral Clustering** while analyzing their performance using **Monte Carlo simulations**.

## Key Objectives

- **Supervised Learning:** Train an ℓ1-penalized **Support Vector Machine (SVM)** for classification.
- **Semi-Supervised Learning:** Implement **self-training**, where an SVM iteratively labels its own data.
- **Unsupervised Learning:** Apply **K-Means clustering** and **Spectral Clustering** for classification.
- **Active Learning:** Train SVMs iteratively with intelligently selected training samples.

## Datasets

### **1️⃣ Breast Cancer Wisconsin Dataset**
- Binary classification task (Benign vs. Malignant).
- 30 numeric attributes extracted from cell nuclei.
- Used for **Supervised, Semi-Supervised, and Unsupervised Learning**.

### **2️⃣ Banknote Authentication Dataset**
- Binary classification problem (Genuine vs. Forged banknotes).
- Features extracted from banknote images using wavelet transforms.
- Used for **Active Learning with SVMs**.

## Methodology

### **1️⃣ Monte Carlo Simulation**
- Each experiment is repeated **30 times** with different random train-test splits.
- **Performance metrics**: **Accuracy, Precision, Recall, F1-Score, AUC**.
- Results are averaged over all runs.

### **2️⃣ Supervised Learning**
- Train an **ℓ1-penalized SVM** with **5-fold cross-validation**.
- Evaluate model performance on both training and test sets.

### **3️⃣ Semi-Supervised Learning (Self-Training)**
- Start with a subset of **labeled data** (50% of positive and negative classes).
- Train an SVM on labeled data.
- Iteratively label the **most uncertain** unlabeled data and retrain.
- Continue until all data is labeled.

### **4️⃣ Unsupervised Learning**
#### **A. K-Means Clustering (k=2)**
- Run multiple iterations with **random initialization** to avoid local minima.
- Use **majority voting** within each cluster to assign class labels.
- Evaluate model performance against true labels.

#### **B. Spectral Clustering**
- Cluster data using **RBF Kernel Spectral Clustering**.
- Choose gamma such that clusters maintain original class balance.
- Compare results with other clustering methods.

### **5️⃣ Active Learning with SVMs**
- Train an SVM with **randomly selected samples**.
- Iteratively add new training samples **based on model uncertainty**.
- Compare accuracy improvements over 50 iterations.

## Results & Insights

- **Supervised SVM** performed best due to access to full labels.
- **Semi-Supervised Learning** improved over time but required careful selection of labeled samples.
- **Unsupervised K-Means & Spectral Clustering** struggled due to lack of label supervision.
- **Active Learning with SVMs** significantly reduced the number of labeled examples needed for good performance.

## Technologies Used

- **Python** (NumPy, Pandas, Matplotlib, Scikit-Learn)
- **Machine Learning**: SVMs, K-Means, Spectral Clustering
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, AUC, Confusion Matrix
- **Cross-Validation & Monte Carlo Simulations** for robust model assessment.

## Future Improvements

- **Test on larger datasets** to evaluate model scalability.
- **Experiment with deep learning approaches** for semi-supervised learning.
- **Optimize active learning strategies** for better sample selection.

## Author

This project was developed as part of **DSCI 552** at the **University of Southern California (USC)**. It demonstrates expertise in **machine learning, classification, active learning, and unsupervised clustering**.

## License

This project is open-source and available under the **MIT License**.
