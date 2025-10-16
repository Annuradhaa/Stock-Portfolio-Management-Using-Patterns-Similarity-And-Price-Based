# Stock-Portfolio-Management-Using-Patterns-Similarity-And-Price-Based
# 📊 Stock Portfolio Management Using Pattern Similarity and Price-Based Clustering

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-Academic-lightgrey)
![Tool](https://img.shields.io/badge/Tool-Google%20Colab-orange)

---

## 🎯 Objective
This project identifies **stocks with similar historical price movement patterns** to a given stock using **Pearson correlation**.  
After identifying similar stocks, they are **clustered by closing prices** within a common range, allowing clearer comparison and informed decision-making.

> 🔍 *Goal:* Segment similarly behaving stocks into meaningful price-based clusters for improved portfolio analysis and investment insights.

---

## 🚀 Run the Project

You can directly open and execute the full code in Google Colab 👇  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1eHaHXbU1tEhTw0i9g6sZFAXc7cir5X4A?usp=sharing)

---

## 🧠 Overview
Financial markets are dynamic and complex. Recognizing stocks that move alike helps investors manage risk and optimize portfolios.  
This project provides a **data-driven approach** combining:

- 📈 **Pearson Correlation** — to detect similar stock movement patterns  
- 🧩 **Hierarchical Clustering** — to group correlated stocks  
- 💰 **Price-Based Segmentation** — to categorize stocks into low, mid, and high price ranges  

Together, these methods help investors identify stocks that are not only behaviorally similar but also financially aligned with their investment range.

---

## ⚙️ Methodology

### 🔹 Phase 1: Data Collection & Preprocessing
- Source: NIFTY 2000 / NIFTY 500 dataset (daily adjusted closing prices)  
- Tools: `pandas`, `yfinance`, `numpy`
- Steps:
  - Handle missing values (forward-fill)
  - Normalize for visualization
  - Store structured data in `.csv` for efficient analysis  

### 🔹 Phase 2: Pattern Similarity (Pearson Correlation)
- Compute correlation between every stock pair  
- Generate a **correlation matrix**  
- Convert to **distance matrix** using:  
  `Distance = 1 - Correlation`

### 🔹 Phase 3: Hierarchical Clustering
- Apply **Agglomerative Linkage**  
- Visualize using a **dendrogram**  
- Determine cluster thresholds dynamically  

### 🔹 Phase 4: Price-Based Grouping
- Find global **min** and **max** closing prices  
- Divide range into segments (Low, Medium, High)  
- Assign each stock to a segment for clear categorization  

---

## 🧩 Tools & Technologies

| Category | Tools / Libraries |
|-----------|------------------|
| **Language** | Python |
| **Data Handling** | pandas, numpy |
| **Visualization** | matplotlib, seaborn |
| **Statistical Analysis** | scipy |
| **Data Source** | yfinance API |
| **Environment** | Jupyter Notebook / Google Colab |

---

## 📈 Results Snapshot

- ✅ Pearson correlation heatmap showing stock relationships  
- ✅ Hierarchical clustering dendrogram  
- ✅ Interactive query tool (Colab-based) for exploring stock similarity  
- ✅ Segmented price groups (Low, Mid, High)  

### Example:
```python
# Example: Find stocks similar to TCS
input_stock = "TCS.NS"
correlation_threshold = 0.6
# Output: Correlated stocks + price group assignment
