# 🏏 K-Means Clustering on Cricket Dataset

## 📌 Overview
This project applies **K-Means Clustering** (unsupervised learning) on a cricket dataset from Kaggle to identify patterns and group similar players based on performance metrics.

## 📂 Dataset
- - Source: Kaggle Cricket Dataset  
- Contains player statistics such as:
  - Matches played
  - Runs scored
  - Batting average
  - Strike rate
  - Wickets (optional)
  - Economy (optional)

---

## ⚙️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn

---

## 🔍 Steps Performed

### 1. Data Preprocessing
- Removed null values  
- Selected relevant numerical features  
- Normalized data using StandardScaler  

### 2. Feature Selection
Example features used:
- Runs
- Batting Average
- Strike Rate

---

### 3. Finding Optimal K
Used **Elbow Method**:
- Compute inertia for different K values  
- Select K where curve bends  

---

### 4. Applying K-Means
```python
from sklearn.cluster import KMeans

kmeans = KMeans(n_clusters=3, random_state=42)
kmeans.fit(X_scaled)
labels = kmeans.labels_
