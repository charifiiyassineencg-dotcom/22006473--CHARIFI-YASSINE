# NOM ET PRENOME : YASSINE CHARIFI 
# Code Apogée : 22006473
![image](https://github.com/charifiiyassineencg-dotcom/DS_2025/blob/main/WhatsApp%20Image%202026-01-05%20at%2014.14.55.jpeg)
# 📘 **RAPPORT DESCRIPTIF – PROJET DATA SCIENCE**

## *Dataset : Diabetes Progression (Régression)*

---

## **1. Contexte & Objectif du Projet**

Le dataset **Diabetes** fourni par *Scikit-Learn* est un jeu de données de référence en Data Science.
Il permet de **prédire la progression quantitative du diabète** chez des patients à partir de mesures cliniques normalisées.

Contrairement à un problème de classification, la variable cible est **continue**, ce qui place ce projet dans un cadre de **régression supervisée**.

### 🎯 **Objectif principal**

Construire une chaîne complète de Machine Learning permettant de :

1. Charger et inspecter le dataset
2. Simuler un cas réel avec des données manquantes
3. Nettoyer et préparer les données
4. Réaliser une analyse exploratoire (EDA)
5. Construire un modèle de régression
6. Évaluer sa performance

---

## **2. Les Données (X et y)**

### 🔹 Variables explicatives (X)

Le dataset contient **10 variables cliniques normalisées**, notamment :

* age – âge du patient
* bmi – indice de masse corporelle
* bp – pression sanguine
* s1 à s6 – mesures sériques liées au métabolisme

Ces variables sont centrées et mises à l’échelle, ce qui facilite l’apprentissage du modèle.

### 🔹 Variable cible (y)

* **Progression du diabète** après un an
* Variable **continue** (régression)

➡️ Le dataset contient **442 observations** et **11 colonnes (10 features + 1 target)**.

---

## **3. Simulation de Données Manquantes (Réalisme du Projet)**

Dans un contexte réel, les données médicales sont souvent incomplètes.
Pour simuler ce scénario :

* **5% de valeurs manquantes** ont été introduites artificiellement
* Uniquement dans les variables explicatives (X)
* La variable cible a été préservée

👉 Cette étape permet de tester la robustesse du pipeline face à des données imparfaites.

---

## **4. Nettoyage & Imputation**

### 🔧 Stratégie utilisée

```python
SimpleImputer(strategy='mean')
```

Pour chaque feature :

* Calcul de la moyenne
* Remplacement des valeurs manquantes par cette moyenne

🔹 Résultat :
**Aucune valeur manquante restante** après l’imputation.

📌 *Note méthodologique*
Dans un contexte industriel strict, l’imputation serait réalisée **après le train/test split** afin d’éviter toute fuite de données (*data leakage*).

---

## **5. Analyse Exploratoire (EDA)**

### 📊 Statistiques descriptives

L’analyse statistique révèle :

* Des variables bien centrées autour de 0
* Des dispersions différentes selon les mesures
* Certaines variables plus informatives que d’autres

### 📉 Distribution de la variable BMI

Le BMI présente :

* Une distribution relativement symétrique
* Une influence notable sur la progression du diabète

Cette variable est reconnue comme **cliniquement pertinente**.

### 🔥 Matrice de corrélation

L’analyse de corrélation montre que :

* **bmi**, **bp** et certaines variables sériques sont fortement corrélées à la cible
* Peu de corrélations extrêmes entre features → faible redondance

---

## **6. Méthodologie de Split (Train/Test)**

```python
train_test_split(test_size=0.2, random_state=42)
```

* **Train** : 80% des données
* **Test** : 20% des données

✔️ Ce ratio permet :

* Un apprentissage stable
* Une évaluation fiable

Le paramètre `random_state=42` garantit la **reproductibilité**.

---

## **7. Modélisation : Random Forest Regressor**

### Pourquoi un Random Forest Regressor ?

* Excellente performance sur des relations non linéaires
* Peu sensible aux outliers
* Capture les interactions complexes entre variables
* Robuste face au bruit

### Paramètres principaux

* `n_estimators = 100`
* `random_state = 42`

Le modèle apprend à approximer la progression du diabète à partir des signaux cliniques.

---

## **8. Évaluation du Modèle**

### 📐 Métriques utilisées

* **Mean Squared Error (MSE)**
  → mesure l’erreur moyenne entre valeurs réelles et prédites

* **R² Score**
  → proportion de la variance expliquée par le modèle

### 📊 Résultats observés

* **MSE modéré**, indiquant des erreurs contrôlées
* **R² ≈ 0.45 – 0.50**, valeur cohérente pour un problème médical réel

### 📈 Visualisation Prédictions vs Réalité

Le nuage de points montre :

* Une tendance linéaire claire
* Une dispersion attendue pour des données biomédicales
* Un modèle globalement bien calibré

---

## **9. Conclusion Générale**

Ce projet démontre la mise en œuvre complète d’un **pipeline de Data Science appliqué à un problème réel de régression** :

1. Chargement des données
2. Simulation de données manquantes
3. Nettoyage et imputation
4. Analyse exploratoire approfondie
5. Séparation méthodologique
6. Modélisation robuste
7. Évaluation pertinente

🎓 **Compétences validées**

* Data cleaning & preprocessing
* Analyse exploratoire
* Gestion des valeurs manquantes
* Régression supervisée
* Interprétation de métriques
* Visualisation des performances

Le dataset **Diabetes** constitue un excellent cas d’étude pour comprendre les limites et les enjeux de la prédiction médicale en Machine Learning.
