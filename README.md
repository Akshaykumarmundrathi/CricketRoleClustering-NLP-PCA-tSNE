# 🏏 Cricket Player Role Classification Using NLP, PCA & t-SNE

This project analyzes cricket players’ descriptions using **Natural Language Processing (NLP)** and unsupervised **dimensionality reduction** techniques. The goal is to extract meaningful features from text, reduce dimensionality, and visualize clustering based on player roles such as **batsmen**, **bowlers**, and **fielders**.

---

## 📂 Dataset

- **File:** `CricketPlayers.csv`
- **Columns:**
  - `Type of Players:` – Role of the player (e.g., Batsman, Bowler, Fielder)
  - `Description:` – A short paragraph describing each player’s career, style, and contribution

> The dataset contains descriptions of 15 top cricket players evenly distributed across the three roles.

---

## 🧠 Project Goals

- Extract relevant textual features from player descriptions
- Convert text into vectors using **TF-IDF**
- Reduce dimensionality using **PCA** and **t-SNE**
- Visualize clustering patterns based on player roles

---

## 📜 Code Workflow

### 1. Load and Prepare Data
- Read the dataset using `pandas`
- Extract columns: `Description:` and `Type of Players:`

### 2. TF-IDF Vectorization
- Apply `TfidfVectorizer` with:
  - 1-gram to 3-gram range
  - Stop word removal
  - Limit of 100 features

### 3. Feature Standardization
- Use `StandardScaler` (with `with_mean=False`) to normalize TF-IDF vectors

`## 📌 Results Summary`:

---

## 📌 Results Summary

This project successfully demonstrates how **descriptive text data** about cricket players can be transformed into meaningful **numerical features** and visualized using unsupervised **dimensionality reduction** techniques.

###  Objective Achieved

We analyzed player descriptions and classified them based on their roles — **batsmen**, **bowlers**, and **fielders** — by using:

* **TF-IDF** for feature extraction
* **PCA** and **t-SNE** for 2D projections
* **Scatter plots** to visualize role-based clustering

---

### 📈 PCA Analysis

* **Explained Variance Plot**:

  * Revealed how much variance is captured by each component.
  * Most variance is preserved in the first few components.

* **MSE vs Component Count**:

  * Shows reconstruction error when reducing features using PCA.
  * Identified an **elbow point**, indicating the **optimal number of components** to retain while preserving information.

---

### 📉 Dimensionality Reduction & Clustering

* **PCA Projection**:

  * Showed partial separation between player types.
  * Captures **global structure** of the TF-IDF space.

* **t-SNE Projection**:

  * Displayed clearer, well-separated clusters for batsmen, bowlers, and fielders.
  * Captures **local neighborhood structure**, revealing more natural groupings.

> ✅ t-SNE outperformed PCA in visually distinguishing player roles from text data.

---

### 🗝️ Keyword Extraction

* TF-IDF identified top keywords from each player’s description.
* Highlighted key traits, play styles, and accomplishments.
* Keywords aligned with the player's designated role.

---

### 🎯 Final Takeaway

This project proves that **unsupervised learning and NLP** techniques can:

* Reveal hidden structure in textual data
* Successfully cluster players by role without labeled features
* Provide interpretable, role-driven insights through visualization

---

- 🔴🔵🟡 **2D Scatter Plots** from PCA and t-SNE showing player type clusters  
  ![Visualization](https://github.com/user-attachments/assets/2f4a4e7c-d89c-4ec0-ba36-5287bbde46e1)

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
