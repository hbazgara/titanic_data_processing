# Projet : Prétraitement de données

## Dataset
Le dataset utilisé est le "Titanic Dataset", téléchargé depuis [Kaggle](https://www.kaggle.com/datasets/yasserh/titanic-dataset).

## Méthodologie

### Exploration (EDA)
Analyse initiale de la structure du dataset : affichage d'un échantillon, identification des valeurs nulles et statistiques descriptives globales.

### Gestion des valeurs manquantes
Stratégie d'imputation pour éviter la perte de données :
* **Numérique :** Remplacement par la médiane.
* **Catégoriel :** Remplacement par le mode (valeur la plus fréquente).

### Correction des types de données
Casting des colonnes vers des types adaptés (ex: `int`, `category`) pour optimiser l'efficacité de Pandas et préparer l'encodage.

### Gestion des outliers (IQR)
Utilisation de l'intervalle interquartile (InterQuartile Range) pour détecter et exclure les valeurs extrêmes, stabilisant ainsi les distributions.

### Encodage (One-Hot Encoding)
Binarisation des variables catégorielles pour permettre leur traitement par les modèles numériques.

## Étapes de réalisation

1.  Affichage des statistiques descriptives.
2.  Imputation des valeurs manquantes de la colonne `Age` par la médiane.
3.  Imputation des valeurs manquantes de `Embarked` par le mode.
4.  Suppression de la colonne `Cabin` (taux de valeurs manquantes trop élevé).
5.  Détection des outliers via la méthode IQR.
6.  Suppression des outliers identifiés dans `Age` et `Fare`.
7.  Conversion des types de données (Casting).
8.  Application du One-Hot Encoding sur les variables catégorielles.
