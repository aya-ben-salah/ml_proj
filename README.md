Description

Ce projet a pour objectif de détecter les transactions frauduleuses par carte bancaire en utilisant des techniques de machine learning.
Il s’inscrit dans un contexte où l’augmentation des paiements numériques s’accompagne d’une hausse des fraudes financières.

Le principal défi est le fort déséquilibre des données, où les transactions frauduleuses représentent une très faible proportion du dataset.


Objectifs

* Analyser un dataset réel de transactions bancaires
* Comprendre les caractéristiques liées à la fraude
* Appliquer des techniques de prétraitement adaptées
* Gérer le déséquilibre des classes (fraude vs non fraude)
* Implémenter plusieurs modèles de classification
* Comparer les performances et choisir le meilleur modèle


Dataset

* Source : Kaggle (Credit Card Fraud Detection)
* Nombre d’observations : 284 807
* Nombre de fraudes : 492 (≈ 0.17%)
* Variables :

  -V1 à V28 : variables transformées (PCA)
  -Time : temps écoulé
  -Amount : montant de la transaction
  -Class : variable cible (0 = normal, 1 = fraude)


Problématique

Le dataset est fortement déséquilibré, ce qui rend certaines métriques comme l’accuracy peu pertinentes.
L’objectif est donc de construire un modèle capable de :

* Détecter un maximum de fraudes (recall élevé)
* Réduire les fausses alertes (bonne précision)


Étapes du projet

1. Analyse exploratoire (EDA)

* Analyse de la variable cible
* Étude des corrélations
* Détection des outliers

2. Prétraitement des données

* Données propres (pas de valeurs manquantes)
* Standardisation
* Séparation train/test (80% / 20%) avec stratification

3. Équilibrage des données

* Random UnderSampling
* SMOTE (génération de données synthétiques)

4. Modélisation

Les modèles utilisés :

* Régression logistique
* K-Nearest Neighbors (KNN)
* Arbre de décision
* Random Forest
* Support Vector Machine (LinearSVC)
* Naive Bayes

5. Évaluation

Les métriques utilisées :

* Precision
* Recall
* F1-score
* AUC
* Matrice de confusion


Résultats

Les performances varient selon les modèles :

- Régression logistique, SVM, Naive Bayes :

  * Recall élevé
  * Précision faible (beaucoup de faux positifs)

- KNN et arbre de décision :

  * Bon compromis entre précision et recall

- Random Forest :

  * Meilleures performances globales
  * Précision ≈ 0.85
  * Recall ≈ 0.85
  * F1-score ≈ 0.85


Conclusion

Le modèle Random Forest est le plus adapté pour ce problème.
Il offre un bon équilibre entre détection des fraudes et réduction des erreurs.


Auteurs

BEN SALAH Aya
