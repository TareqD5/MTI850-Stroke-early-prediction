# Système de Prédiction d'AVC

## Présentation du Projet
Ce projet vise à développer un outil analytique capable d'évaluer la probabilité qu'un patient subisse un accident vasculaire cérébral (AVC) en fonction de facteurs démographiques et médicaux. Selon l'OMS, les AVC sont la troisième cause de décès et d'invalidité dans le monde. 

L'intérêt principal de ce projet est l'utilisation de **Big Data Analytics** pour traiter et modéliser des données de santé à grande échelle en utilisant l'écosystème **Apache Spark**.

## Données
Le projet utilise le jeu de données "Kaggle Stroke Prediction Dataset".
- **Volume** : ~5 110 enregistrements (augmentés par synthèse pour simuler un contexte Big Data).
- **Cible** : `stroke` (Indicateur binaire).
- **Caractéristiques clés** : Genre, âge, hypertension, maladies cardiaques, statut matrimonial, type de travail, niveau de glucose, IMC et statut de fumeur.

## Technologies Utilisées
- **Langage** : Python
- **Traitement de données** : PySpark (Spark SQL & MLlib), Pandas, NumPy
- **Visualisation** : Matplotlib, Seaborn
- **Modélisation** : Logistic Regression, Random Forest, GBT Classifier
- **Infrastructure** : Google Colab / Hadoop HDFS

## Fonctionnalités
1. **Data Augmentation** : Simulation de données massives avec ajout de bruit et de valeurs manquantes pour tester la robustesse des pipelines.
2. **Prétraitement & Nettoyage** : Imputation de valeurs manquantes (Moyenne/Mode), encodage des variables catégorielles (StringIndexer, OneHotEncoder).
3. **Analyse Exploratoire (EDA)** : Visualisation des corrélations et des distributions des variables médicales.
4. **Machine Learning** : 
   - Gestion du déséquilibre des classes (Oversampling & Class Weights).
   - Évaluation via AUC-ROC et Recall.
   - Modèle **Random Forest** optimisé avec un Recall de **~86%** pour la détection des cas positifs.
5. **Pipeline de Production** : Création d'un pipeline Spark complet exportable pour des prédictions en temps réel.
6. **Streaming (Simulation)** : Mise en place d'un flux de données structuré pour simuler l'arrivée de données de patients en continu.

## Structure du Notebook
- **Section 1-3** : Configuration de Spark et exploration initiale.
- **Section 4-5** : Visualisation des données et ingénierie des variables.
- **Section 6** : Gestion du stockage (Parquet, HDFS).
- **Section 7-8** : Modélisation, comparaison des algorithmes et sauvegarde des modèles.
- **Section 9-10** : Déploiement du Pipeline et test sur flux de données (Streaming).

## Équipe
Projet réalisé par :
- Fatima IGUEROUFA
- Louis-Philippe ROBICHAUD
- Tareq DERDAKI

---
*Référence : [1] World Health Organization (WHO). Global Health Estimates.*
