# 🏏 Cricket Player Role Classification Using NLP, PCA & t-SNE

This project analyzes cricket players’ descriptions using **Natural Language Processing (NLP)** and unsupervised **dimensionality reduction** techniques. The goal is to extract meaningful features from text, reduce the dimensionality of the dataset, and visualize clustering based on player roles such as **batsmen**, **bowlers**, and **fielders**.

---

## 📂 Dataset

- **File:** `CricketPlayers.csv`
- **Columns:**
  - `Type of Players:` – Role of the player (e.g., Batsman, Bowler, Fielder)
  - `Description:` – A short paragraph describing each player (career, style, contribution)

The dataset contains textual descriptions of 15 cricket players, evenly distributed among the 3 roles.

---

## 🧠 Purpose

The primary objective is to:
- Extract relevant textual features from player descriptions
- Use **TF-IDF** to numerically represent descriptions
- Apply **Principal Component Analysis (PCA)** and **t-SNE** to reduce features
- Visualize and compare clustering patterns among player types

---

## 📜 Code Workflow

### 1. Load and Prepare Data
- Read the CSV file using pandas
- Extract the `Description:` and `Type of Players:` columns

### 2. TF-IDF Vectorization
- Use `TfidfVectorizer` to transform descriptions into numerical feature vectors
- Use n-grams (1 to 3), remove stop words, and limit to 100 features

### 3. Feature Standardization
- Apply `StandardScaler` (with_mean=False) to normalize the TF-IDF vectors

### 4. Dimensionality Reduction
- Apply **PCA** to:
  - Calculate explained variance ratios
  - Visualize optimal number of components
  - Reconstruct TF-IDF matrix and compute **Mean Squared Error (MSE)**
- Plot **MSE vs Number of Components** to evaluate compression loss

### 5. Visualization
- Reduce to 2D using:
  - **PCA**: For linear relationships
  - **t-SNE**: For non-linear structure
- Generate scatter plots color-coded by player roles

### 6. Keyword Extraction
- Extract the most influential words from each description based on non-zero TF-IDF weights

---

## 📊 Output Visuals

- 📈 **Explained Variance Plot** for PCA
- 📉 **MSE vs. Component Count** plot
- 🔴🔵🟡 **2D Scatter Plots** using PCA and t-SNE for role-based clustering

---

## 📁 Project Structure

-  CricketPlayers.csv  **Dataset**
-  cricket_role_clustering.py  **Python script** containing all logic
-  README.md   **This file**


---

## ⚙️ Requirements

```bash
pip install pandas scikit-learn matplotlib
```
