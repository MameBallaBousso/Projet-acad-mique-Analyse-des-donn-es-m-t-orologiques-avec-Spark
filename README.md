# Projet-acad-mique-Analyse-des-donn-es-m-t-orologiques-avec-Spark

📊 Analyse des données météorologiques et agricoles avec Spark
👥 Membres du groupe

Mame Balla Bousso

Cheikh Oumar Diallo

Samba Dieng

Raherinasolo Ange Emilson Rayan

Albert Zinaba

🎯 Thème du projet

Analyse des données météorologiques avec Apache Spark et étude de leur impact sur les rendements agricoles au Sénégal

🗂️ Sources des données
🌦️ Données météorologiques

Source : NASA Power

Contenu : données journalières de température

Utilisation : analyse, apurement et transformation des données climatiques

🌾 Données agricoles

Source : Sénégal Open Data

Contenu : rendements agricoles annuels par culture et par région

Utilisation : analyse économétrique et mise en relation avec les variables climatiques

🛠️ Technologies utilisées

Apache Spark (PySpark)

Python

Jupyter Notebook

Amazon S3 (stockage intermédiaire des données)

Outils de visualisation (matplotlib, seaborn, etc.)

📁 Organisation du projet

Le projet est structuré autour de trois notebooks principaux, chacun correspondant à une étape clé du pipeline de traitement et d’analyse des données.

🔹 1. 01_ingestion_profiling_meteo.ipynb

Téléchargement et ingestion de la base météorologique

Apurement et nettoyage initial de la base météo

Calcul de statistiques descriptives

Premières visualisations exploratoires des données de température

Ce notebook permet de comprendre la structure et la qualité des données météorologiques

Les visualisations approfondies sont destinées à être reprises dans un dashboard ultérieur

🔹 2. 01_claning_for_modeling.ipynb

Transformation des données météorologiques

Agrégation des températures journalières en données saisonnières

Calcul d’indicateurs climatiques adaptés à l’analyse agricole

Objectif principal : rendre les données météorologiques compatibles avec les données annuelles de rendements agricoles

Sauvegarde de la base transformée dans un bucket Amazon S3

🔹 3. modeling.ipynb

Chargement de la base météorologique transformée

Fusion (merge) avec la base de rendements agricoles par culture et par région

Construction d’une base finale d’analyse

Mise en place d’une modélisation économétrique en données de panel

Analyse de l’impact des variables climatiques sur les rendements agricoles

⚠️ Particularité : dans ce notebook, la base finale a été directement téléchargée après transformation puis mergée avec la base agricole.

🔄 Gestion des données et interconnexion des notebooks

À chaque étape clé, les données intermédiaires sont :

enregistrées dans un bucket Amazon S3

puis rechargées dans le notebook suivant via un lien vers ce bucket

Cette approche garantit :

la reproductibilité

la traçabilité

la séparation claire des étapes du projet

📈 Résultats attendus

Une base de données consolidée combinant climat et agriculture

Une analyse descriptive et visuelle des températures

Une modélisation économétrique permettant d’évaluer l’impact des conditions météorologiques sur les rendements agricoles au Sénégal
📊 Dashboard (Databricks)

Un dashboard interactif a été développé directement avec Databricks.

Il comprend :

un onglet montrant l’évolution conjointe des variables économiques (rendements agricoles) et des indicateurs climatiques ;

des onglets dédiés à l’évolution des variables de température et autres indicateurs météorologiques.

Le dashboard permet une lecture synthétique et visuelle des relations entre climat et agriculture.
