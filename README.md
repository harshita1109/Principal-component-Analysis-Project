 **Welcome to the PCA Project!**  
This project demonstrates how **Principal Component Analysis (PCA)** can be used to **reduce the dimensionality** of high-dimensional data while preserving as much variance (information) as possible.  

📘 **Dataset Used:** `Digits Dataset` from **Scikit-learn**

---

## 🎯 Project Overview

PCA is a **statistical technique** used for:
- 🧩 Reducing dimensions of large datasets
- 📉 Improving visualization
- ⚙️ Optimizing model performance by removing redundant features

This project walks through:
1. 🔹 Standardizing the data  
2. 🔹 Computing the covariance matrix  
3. 🔹 Finding **Eigenvalues** and **Eigenvectors**  
4. 🔹 Selecting top principal components  
5. 🔹 Visualizing the explained variance  
6. 🔹 Applying PCA for **Logistic Regression** classification

---

## 🧾 Step-by-Step Process

### 1️⃣ Data Preparation
- Load the **Digits Dataset**
- Convert it into a pandas DataFrame
- Visualize the first few digits using `matplotlib`

### 2️⃣ Standardization
Standardize the data to ensure each feature contributes equally:  
> Mean = 0, Standard Deviation = 1

### 3️⃣ Covariance Matrix
Compute the covariance matrix to understand relationships between features.

### 4️⃣ Eigenvalues & Eigenvectors
- 🧮 **Eigenvectors** indicate the directions of maximum variance.
- 📈 **Eigenvalues** represent the magnitude of variance captured in each direction.

### 5️⃣ Explained Variance
Visualize how much variance is captured by each principal component.

```python
plt.bar(range(len(var_exp)), var_exp, label='Individual Explained Variance', color='g')
plt.step(range(len(cumulative_var_exp)), cumulative_var_exp, label='Cumulative Variance')
plt.xlabel('Principal Component Index')
plt.ylabel('Explained Variance Ratio')
plt.legend()
plt.show()
```

### 6️⃣ Dimensionality Reduction & Classification
- Reduce dimensions using PCA (`PCA(0.95)` → keeps 95% variance)
- Train a **Logistic Regression** classifier
- Evaluate accuracy 📊

---

## 🧰 Tech Stack

| Tool / Library | Description |
|-----------------|--------------|
| 🐍 **Python** | Programming Language |
| 🧮 **NumPy** | Mathematical operations |
| 🧾 **Pandas** | Data manipulation |
| 📊 **Matplotlib** | Data visualization |
| 🧠 **Scikit-learn** | ML algorithms & PCA implementation |

---

## 🧠 Results

✅ **Dimensionality reduced** from original features to fewer principal components (capturing 95% of variance).  
✅ **Accuracy achieved:** around **97–99%** (depending on components used).  
✅ **Significant computational efficiency** gain without much loss in performance.

---

## 📸 Sample Outputs

### 🔍 Visualizing First 5 Digits:
```python
for x in range(5):
  plt.gray()
  plt.matshow(dataset.data[x].reshape(8,8))
  plt.show()
```

🖼️ The project displays sample images of digits from the dataset and their corresponding targets.

---

## 🚀 Future Enhancements

✨ Try PCA on larger datasets  
📈 Compare PCA with t-SNE or LDA  
🤖 Apply PCA-transformed data on other ML models like SVM or Random Forest

---

## 🧑‍💻 Author

👋 **Developed by:** Harshita Sharma
💬 *“Dimensionality reduction is not just about smaller data — it’s about smarter data!”*

📬 **Reach out on GitHub or LinkedIn for collaboration opportunities!**

---

## 🌟 Show Your Support

If you liked this project:
- ⭐ **Star this repo**
- 🍴 **Fork it** and try your own experiments
- 🧩 **Contribute** to improve it!

---

## 📚 References
- [Scikit-learn PCA Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)
- [Digits Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_digits.html)
