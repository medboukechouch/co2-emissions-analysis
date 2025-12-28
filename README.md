# Analyse des Émissions de CO2 des Véhicules 🚗💨

Ce projet a pour objectif d'analyser les facteurs influençant les émissions de dioxyde de carbone (CO2) des véhicules. À travers une approche structurée (nettoyage, analyses univariée, bivariée et multivariée), nous explorons les relations entre les caractéristiques techniques des voitures (taille du moteur, cylindres, consommation) et leur impact environnemental.

## 📂 Structure du Projet

Le projet est organisé autour de plusieurs notebooks Jupyter, suivant une progression logique de l'analyse de données :

### 1. Préparation des données
- **Fichier :** `Nettoyage_des_données.ipynb`
- **Description :** Traitement du jeu de données brut (`co2.csv`).
- **Actions clés :**
  - Suppression des doublons et des valeurs manquantes.
  - Renommage des colonnes pour une meilleure lisibilité.
  - **Résultat :** Passage de 7385 à 6282 entrées (1103 lignes supprimées) pour garantir la qualité des données. Export vers `Co2_Nettoye.csv`.

### 2. Analyse Monovariée
- **Fichier :** `Analyse_monovarié.ipynb`
- **Description :** Étude de la distribution de chaque variable individuellement.
- **Contenu :** Statistiques descriptives (moyenne, médiane, écart-type, skewness, kurtosis) et visualisation des distributions pour comprendre les tendances générales du parc automobile analysé.

### 3. Analyse Bivariée
- **Fichier :** `Analyse_bivariée.ipynb`
- **Description :** Exploration des relations entre deux variables.
- **Méthodes :**
  - Corrélations (Matrice de corrélation).
  - Tests statistiques (ANOVA, Chi-2).
  - Visualisations (Scatterplots, Boxplots) pour identifier les liens forts (ex: relation entre la taille du moteur et la consommation).

### 4. Analyse Multivariée
- **Fichier :** `Analyse multivarié.ipynb`
- **Description :** Analyse globale des relations entre toutes les variables simultanément.
- **Méthode principale :** Analyse en Composantes Principales (ACP/PCA).
  - **Résultats clés :** 7 variables analysées. Les deux premiers axes (F1 + F2) expliquent environ **95.48%** de l'inertie, ce qui permet une excellente représentation des données en 2 dimensions.

## 📊 Données

- **Source :** `co2.csv` (Données brutes)
- **Données nettoyées :** `Co2_Nettoye.csv`
- **Principales variables :**
  - `Make`, `Model`, `Vehicle_Class` (Catégorielles)
  - `Engine_Size_L`, `Cylinders` (Moteur)
  - `Fuel_Consumption_*` (Consommation Ville/Autoroute)
  - `CO2_Emissions_gkm` (Variable cible)

## 🛠️ Technologies utilisées

Le projet est réalisé en **Python** avec les bibliothèques suivantes :
- **Pandas** & **NumPy** : Manipulation et nettoyage des données.
- **Matplotlib** & **Seaborn** : Visualisation de données.
- **Scikit-learn** : Pré-traitement et Analyse en Composantes Principales (PCA).
- **SciPy** : Tests statistiques (Pearson, Chi-2, etc.).

## 🚀 Comment utiliser ce projet

1. Clonez ce dépôt :
   ```bash
   git clone [https://github.com/votre-nom-utilisateur/nom-du-projet.git](https://github.com/votre-nom-utilisateur/nom-du-projet.git)
   
