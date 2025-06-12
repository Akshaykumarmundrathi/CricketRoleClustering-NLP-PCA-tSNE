# CricketRoleClustering-NLP-PCA-tSNE
A project that uses TF-IDF, PCA, and t-SNE to extract, reduce, and visualize features from cricket players' textual descriptions to classify them into roles like batsmen, bowlers, and fielders.

---

````markdown
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

## 📜 Code Structure

```python
1. Load Dataset
   - Read the CSV file using pandas.
   - Extract 'Description' and 'Type of Players' columns.

2. Text Vectorization with TF-IDF
   - Use TfidfVectorizer to extract n-gram features from descriptions.
   - Limit to 100 features with filtering based on term frequency.

3. Feature Standardization
   - StandardScaler (with_mean=False) is used to standardize TF-IDF vectors.

4. Dimensionality Reduction with PCA
   - Apply PCA to calculate explained variance.
   - Select optimal number of components (k = 9).
   - Reconstruct the TF-IDF matrix and compute Mean Squared Error (MSE).

5. MSE vs Component Count
   - Plot reconstruction loss to justify the number of components retained.

6. PCA and t-SNE Visualization
   - Reduce to 2 components using both PCA and t-SNE.
   - Plot 2D scatter plots color-coded by player type.

7. Feature Extraction Insight
   - Extract keywords used for each player based on non-zero TF-IDF scores.
````

---

## 📊 Visual Outputs

* **Explained Variance Plot (PCA):** Shows how much variance is retained as more components are added.
* **MSE Plot:** Shows reconstruction error for each k from 1 to 13.
* **2D Scatter Plots:**

  * PCA Projection (Linear)
  * t-SNE Projection (Non-linear)
  * Both show clear grouping of players by role.

---

## 🔧 Requirements

* Python 3.7+
* Libraries:

  * pandas
  * scikit-learn
  * matplotlib
  * seaborn (optional for improved plotting)

Install dependencies with:

```bash
pip install pandas scikit-learn matplotlib
```

---

## 📌 Conclusion

This project demonstrates how **NLP and unsupervised learning techniques** like **PCA** and **t-SNE** can uncover structure and patterns in text data. It can be extended to larger datasets, different player categories, or adapted for other domains such as movie reviews, product descriptions, etc.

---

## 📁 Folder Structure

```
├── CricketPlayers.csv         # Dataset file
├── cricket_role_clustering.py # Main code script
├── README.md                  # Project documentation
```

---

## 🙌 Acknowledgements

This project is built as an academic or learning exercise to explore the power of dimensionality reduction and textual feature extraction.

```

Let me know if you'd like this converted to a `.ipynb` version or want GitHub badges or screenshots added!
```
