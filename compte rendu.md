# NOM ET PRENOME : YASSINE CHARIFI 
# Code Apogée : 22006473

# 📊 Projet de Prédiction – Dataset Diabetes

## Description du projet

Ce projet a pour objectif de **prédire la progression du diabète** chez des patients à partir de variables cliniques. Il couvre l'ensemble du **cycle de vie d'un projet Data Science**, depuis l'importation des données jusqu'à l'évaluation d'un modèle de Machine Learning.

---

## Technologies et Bibliothèques

* Python 3.x
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-Learn

---

## Structure du projet

```text
├── notebooks/
│   └── diabetes_regression.ipynb  # Notebook principal
├── src/
│   └── preprocessing.py           # Scripts de nettoyage et préparation
├── README.md                      # Ce fichier
└── requirements.txt               # Bibliothèques nécessaires
```

---

## Étapes du projet

### 1. Chargement des données

* Dataset : `load_diabetes` de Scikit-Learn
* Variables : 10 features cliniques
* Target : progression du diabète (valeur continue)

### 2. Pré-traitement

* Introduction de 5% de valeurs manquantes artificiellement
* Imputation des valeurs manquantes par la moyenne

### 3. Analyse Exploratoire (EDA)

* Statistiques descriptives
* Distribution de la variable `bmi`
* Matrice de corrélation des 10 premières features

### 4. Séparation Train / Test

* 80% données entraînement
* 20% données test

### 5. Modélisation

* Modèle : **Random Forest Regressor**
* Entraînement sur les données d'entraînement

### 6. Évaluation

* **Mean Squared Error (MSE)** : 3013.12
* **R-squared (R²)** : 0.46

**Graphique : Prédictions vs Réalité**

![Prédictions vs Réalité](https://via.placeholder.com/600x400?text=Graph+Predictions+vs+Reality)

---

## Conclusion

Le modèle Random Forest Regressor offre une **prédiction raisonnable** de la progression du diabète.
Points clés :

* Bon traitement des données manquantes
* Analyse exploratoire détaillée
* Séparation Train/Test et évaluation rigoureuse

---

## Pour aller plus loin

* Tester d’autres modèles : Lasso, Ridge, Gradient Boosting
* Optimisation d’hyperparamètres avec GridSearchCV
* Déploiement du modèle avec Streamlit ou Flask

---

## Licence

MIT License

---

Si tu veux, je peux te faire **une version encore plus pro avec badges GitHub, graphiques intégrés et sections “Usage” et “Installation”**, prête à mettre sur ton dépôt.

Veux‑tu que je fasse ça ?
