## Projet_cloud_modern_data_stack : PostgreSQL → S3 → Snowflake → dbt → Airflow → Power BI

## Objectifs
Mettre en place un pipeline Cloud complet reproduisant l'architecture du Modern Data Stack :
- Extraction de la donnée transactionnelle PostgreSQL
- Stockage des données brutes dans Amazon S3
- Ingestion et transformation dans Snowflake (Data Warehouse)
- Orchestration des traitements via Apache Airflow
- Modélisation analytique et création de Data Marts avec dbt
- Reporting interactif Power BI

## Technologies utilisées
- PostgreSQL (OLTP source)
- Amazon S3 (stockage cloud)
- Snowflake (Data Warehouse cloud)
- dbt (Data Build Tool, transformations analytiques)
- Apache Airflow (orchestration)
- Power BI (visualisation et reporting)

## Structure du dépôt
- **/sql/** : scripts SQL de création de tables et génération de données sur PostgreSQL, scripts ou notebook d’export vers CSV/S3
- **/scripts/** : scripts SQL de génération de données sur PostgreSQL, et d’export vers CSV/S3
- **/dbt/** : projet dbt complet (modèles, seeds, analyses)
- **/powerbi/** : fichiers Power BI et screenshots des dashboards
- **rapport.pdf** : rapport détaillant la démarche, choix, résultats, problèmes/dépannage éventuels

## Instructions pour exécuter le projet

1. **Installer/configurer chaque composant (PostgreSQL, S3, Snowflake, dbt, Airflow, Power BI).**
2. **Charger les données démo dans PostgreSQL** à l’aide des scripts du dossier `/postgres/`
3. **Exporter les données PostgreSQL vers S3** (voir `/postgres/export_to_s3.py` ou tutoriel)
4. **Créer votre Data Warehouse Snowflake, créer les tables et charger les données depuis S3** (`/snowflake/`)
5. **Configurer et déployer le projet dbt** (dans `/dbt/`) sur Snowflake, exécuter les transformations, générer les data marts
6. **Automatiser le pipeline** avec les DAGs Airflow (`/airflow/`)
7. **Connecter Power BI** à Snowflake et créer vos visualisations (capturer les principaux rapports en images si besoin)
8. **Voir le rapport pour tout détail, approche ou difficultés rencontrées**

## Membres du groupe
- Khadija Nachid Idrissi
- Rajae Fdili
- Aya Hamim
