# 🧠 Customer Segmentation & Product Recommendation using KNN

This project uses **unsupervised learning (KMeans)** for customer segmentation and **collaborative filtering (KNN)** for personalized product recommendations, based on historical transaction data from an e-commerce retail dataset.

---

## 🚀 Project Goals

- Segment customers based on **Recency, Frequency, and Monetary (RFM)** values
- Cluster customers using **KMeans**
- Recommend products to a customer based on similar users using **K-Nearest Neighbors (KNN)** collaborative filtering

---

## 📁 Dataset

- **Columns**: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## 🔧 Tech Stack

| Tool / Library | Use |
|----------------|-----|
| `Python` | Programming |
| `Pandas`, `NumPy` | Data manipulation |
| `Matplotlib`, `Seaborn` | EDA & Visualization |
| `Scikit-learn` | ML Models (KMeans, KNN, Metrics) |
| `Streamlit` | Web App UI (optional) |

---

## 📊 Exploratory Data Analysis (EDA)

- Cleaned missing values, removed negative quantities
- Created RFM features:
  - **Recency**: Days since last purchase
  - **Frequency**: Number of orders
  - **Monetary**: Total spend
- Visualized correlations and customer distribution

---

## 📈 Model Building

### 🧩 1. KMeans Clustering

- Scaled RFM data using `StandardScaler`
- Applied `KMeans` clustering (optimal K via elbow method or silhouette score)
- Assigned each customer to a cluster

### 🤝 2. KNN Collaborative Filtering

- Built a **Customer × Product** matrix
- For a given customer:
  - Found similar customers using KNN (`cosine` distance)
  - Recommended products they bought that the target customer hasn’t yet

---

## Results

- Customers were effectively segmented into behavioral clusters.
- Personalized product recommendations were generated using similarity-based filtering.
