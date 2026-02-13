# 🚀 Pipeline ETL - Offres d'Emploi IA/ML France

![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD8?style=for-the-badge&logo=delta&logoColor=white)

## 📋 Description

Pipeline ETL (Extract, Transform, Load) développé sur **Databricks** pour analyser le marché de l'emploi en Intelligence Artificielle et Machine Learning en France.

### 🎯 Objectifs
- Extraire les données d'offres d'emploi depuis l'API France Travail
- Nettoyer et transformer les données avec PySpark
- Créer des agrégations analytiques (par région, par type de contrat)
- Stocker les résultats en format **Delta Lake**

---

## 📊 Résultats du Pipeline

| Métrique | Valeur |
|----------|--------|
| 📥 Données brutes | 6 229 offres |
| ✅ Après nettoyage | 5 096 offres |
| 🗑️ Doublons supprimés | 1 133 |
| 📦 Tables Delta créées | 3 |

---

## 🏗️ Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   API France    │────▶│   Databricks    │────▶│   Delta Lake    │
│    Travail      │     │    PySpark      │     │    Tables       │
└─────────────────┘     └─────────────────┘     └─────────────────┘
      EXTRACT              TRANSFORM                 LOAD
```

---

## 📁 Tables Delta Créées

### 1. `offres_emploi_ia`
Table principale avec toutes les offres nettoyées (5 096 lignes, 20 colonnes)

### 2. `offres_par_region`
Agrégation du nombre d'offres par région française

### 3. `offres_par_contrat`
Agrégation du nombre d'offres par type de contrat (CDI, CDD, Intérim...)

---

## 🛠️ Technologies Utilisées

- **Databricks** - Plateforme Big Data & Analytics
- **PySpark** - Traitement distribué des données
- **Delta Lake** - Format de stockage ACID
- **Python** - Langage de programmation
- **API France Travail** - Source des données (OAuth2)

---

## 📈 Insights Clés

### 🗺️ Top 5 Régions
1. Île-de-France
2. Occitanie
3. Auvergne-Rhône-Alpes
4. PACA
5. Nouvelle-Aquitaine

### 📝 Types de Contrat
- **CDI** : Majoritaire (~80%)
- **CDD** : Variable (6-36 mois)
- **Intérim** : Court terme

---

## 🚀 Comment Exécuter

### Prérequis
- Compte Databricks (Community Edition gratuit)
- Fichier CSV des offres d'emploi

### Étapes
1. Créer un Volume dans Databricks Catalog
2. Uploader le fichier CSV
3. Importer le notebook `ETL_Offres_Emploi_IA.py`
4. Exécuter toutes les cellules

---

## 📂 Structure du Projet

```
databricks-etl-emploi/
├── ETL_Offres_Emploi_IA.py    # Notebook principal
├── README.md                   # Documentation
├── screenshots/                # Captures d'écran
│   ├── pipeline_result.png
│   └── delta_tables.png
└── data/
    └── offres_sample.csv       # Échantillon de données
```

---

## 👤 Auteur

**Yasser Barrada**
- 🌐 [Portfolio](https://barrada-yasser.github.io)
- 💼 [LinkedIn](https://linkedin.com/in/yasser-barrada)
- 🐙 [GitHub](https://github.com/Barrada-yasser)

---

## 📄 Licence

Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 🔗 Projets Connexes

- [Dashboard Power BI - Recrutement IA/ML](https://github.com/Barrada-yasser/dashboard-recrutement-ia)
- [Script Python - API France Travail](https://github.com/Barrada-yasser/api-france-travail)
