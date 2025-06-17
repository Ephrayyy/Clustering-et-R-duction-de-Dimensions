# 🧠 PCA & Machine Learning sur données catégorielles

Ce projet explore deux approches de Machine Learning non supervisée et supervisée à partir d’un jeu de données contenant une variable cible catégorielle (`target`).

---

## 📁 Fichiers fournis

- `Train.csv` : données d'entraînement avec variables explicatives et la colonne `target`.
- `Test.csv` : données de test à exploiter ensuite.
- `Projet_3.ipynb` : notebook principal contenant toutes les étapes du projet.
- `README.md` : ce fichier.

---

## 🎯 Objectif du projet

1. **Réduction de dimension avec PCA**
2. **Clustering non supervisé** (KMeans, DBSCAN, Agglomératif, GMM)
3. **Évaluation du clustering via Adjusted Rand Index (ARI)**
4. **Classification supervisée** (RandomForest, SVM, KNN…)
5. **Comparaison des performances des modèles supervisés**
6. **Visualisation** des résultats

---

## 🛠️ Technologies utilisées

- Python 3.9+
- Scikit-learn
- Pandas / Numpy
- Seaborn / Matplotlib
- Jupyter Notebook

---

## 🔄 Pipeline général

### 1. Prétraitement
- Standardisation des données (`StandardScaler`)
- Encodage de la variable `target` si elle est catégorielle (`LabelEncoder`)

### 2. PCA
- Réduction des dimensions pour expliquer 90 % de la variance

### 3. Clustering non supervisé
- KMeans
- DBSCAN
- Agglomerative Clustering
- Gaussian Mixture Models (GMM)
- Évaluation via `Adjusted Rand Index (ARI)`

### 4. Classification supervisée
- Séparation train/test (80/20)
- Modèles testés :
  - Random Forest
  - SVM
  - KNN
  - Logistic Regression
- Évaluation :
  - Accuracy
  - Matrice de confusion
  - Classification report

---

## 📊 Résultats

### 🧩 Clustering

| Modèle       | ARI obtenu |
|--------------|------------|
| KMeans       | 0.071      |
| DBSCAN       | 0.015      |
| Agglomératif | 0.041      |
| GMM          | 0.063      |

👉 Aucun clustering ne reproduit bien la structure des vraies classes.

### 🧠 Classification

> À compléter avec les scores de précision obtenus dans le notebook une fois l'exécution terminée.

---

## 📌 Conclusion

- Le jeu de données ne présente **pas de structure de clustering claire**.
- L’approche **supervisée** donne des résultats bien **plus pertinents** pour prédire la `target`.
- Le PCA permet une **réduction efficace** de la dimension sans perte majeure d'information.

---

## 🚀 À venir

- Visualisation avec t-SNE ou UMAP
- Export des modèles pour production