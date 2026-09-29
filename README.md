# BCG x Forage — Data Science Job Simulation

Simulation Data Science réalisée sur la plateforme Forage, dans le cadre du programme Boston Consulting Group (BCG) GenAI Data Science.

## Contexte

PowerCo, une entreprise du secteur de l'énergie (électricité et gaz), fait face à un taux de désabonnement (churn) élevé sur sa clientèle PME. L'hypothèse du client est que ce churn est déterminé par la sensibilité des clients aux prix.

L'objectif de la mission : tester cette hypothèse, construire un modèle prédictif du churn, et formuler des recommandations actionnables.

## Démarche

### 1. Analyse exploratoire des données (EDA)

Exploration de trois jeux de données fournis par le client : données client historiques, données de tarification historiques (prix fixes et variables) et indicateur de désabonnement. Étude des types de données, statistiques descriptives et distributions pour comprendre la structure et la qualité des données.

### 2. Feature Engineering

Construction de fonctionnalités permettant de mesurer la sensibilité aux prix (élasticité-prix de la demande) et de tester l'hypothèse du client, à partir des données de consommation et de tarification.

### 3. Modélisation

Test de l'hypothèse à l'aide d'un modèle de classification binaire (Random Forest), avec arbitrage entre complexité, explicabilité et précision. Le modèle final atteint 90% de précision.

## Résultats clés

- **Churn confirmé et élevé** : 9,7% sur 14 606 clients dans la division PME
- **L'hypothèse initiale du client est infirmée** : la sensibilité au prix n'est pas le principal facteur de churn. Les trois variables les plus déterminantes sont la consommation annuelle, la consommation prévisionnelle et la marge nette
- **Recommandation** : une stratégie de remise de 20% est efficace, mais uniquement si elle cible les clients à forte valeur et à forte probabilité de désabonnement

## Contenu du dépôt

- `client_data.csv`, `price_data.csv` — données sources fournies par le client
- `Data Description.pdf` — description des colonnes des jeux de données
- `clean_data_after_eda.csv` — données nettoyées après l'analyse exploratoire
- `data_for_predictions.csv` — données prêtes pour la modélisation, après feature engineering
- `out_of_sample_predictions.csv` — prédictions du modèle sur le jeu de test
- `Tache_2_EDA.ipynb` — analyse exploratoire des données
- `Tache_3_Feature_Engineering.ipynb` — construction des fonctionnalités
- `Tache_4_Modeling.ipynb` — modélisation et évaluation
- `Executive_Summary.pdf` — synthèse des résultats et recommandations
  
## Stack technique

Python, Pandas, NumPy, scikit-learn (Random Forest), Google Colab

---
