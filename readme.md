# Projet Power BI : AtlasDistrib — Du nettoyage des données au tableau de bord commercial

##  Description du projet
Ce projet consiste à concevoir et développer de bout en bout une solution de Business Intelligence (BI) sous **Power BI Desktop** pour l'entreprise **AtlasDistrib SARL** (distributeur de matériel informatique, téléphonie, électroménager et image & son basé à Casablanca). 

L'objectif principal est de remplacer le reporting mensuel manuel sur Excel par un tableau de bord dynamique et interactif destiné au comité de direction (et notamment à Mme Samira Kadiri, Directrice Commerciale). Le projet couvre l'ensemble du cycle de vie de la donnée :
1. **Extraction, Transformation et Chargement (ETL)** avec **Power Query** à partir de sources brutes hétérogènes (export CSV de l'ancien ERP 2024, export Excel du nouvel ERP 2025, référentiels mis en forme et objectifs croisés).
2. **Modélisation sémantique** en constellation (2 tables de faits `Ventes` et `Objectifs` reliées à 4 tables de dimensions `Calendrier`, `Produits`, `Clients`, `Commerciaux`) et création de 15 mesures analytiques en **DAX**.
3. **Data Visualisation** répartie sur 5 pages de rapport (Synthèse, Produits, Clients et territoires, Performance commerciale 2025, et Fiche produit en extraction) pour répondre aux 7 questions métier stratégiques.

---

## 📁 Structure du projet
```text
TP_AtlasDistrib/
│
├── 📂 data/                           # Dossier des données sources brutes (TP_AtlasDistrib_Donnees)
│   ├── Ventes_2024.csv                # Historique des ventes 2024 (Ancien ERP, séparateur ';', UTF-8)
│   ├── Ventes_2025.xlsx               # Ventes 2025 (Nouvel ERP, feuille 'Export_ERP')
│   ├── Referentiels.xlsx              # Tables de dimensions (Produits, Clients, Villes, Commerciaux)
│   └── Objectifs_2025.xlsx            # Objectifs mensuels par commercial (format tableau croisé)
│
├── 📂 powerbi/                        # Fichiers de travail Power BI
│   └── AtlasDistrib_NomPrenom.pbix    # Modèle de données, requêtes Power Query et rapport complet
│
├── 📂 docs/                           # Documentation et livrables écrits
│   ├── TP_PowerBI_AtlasDistrib.pdf    # Énoncé et cahier des charges du TP
│   └── Fiche_Reponses_AtlasDistrib.pdf# Journal de nettoyage, réponses Q1-Q7 et limites d'analyse
│
├── README.md                          # Documentation principale du projet (ce fichier)
└── project_metadata.txt               # Métadonnées du projet en anglais (Auteur, Dates, Version)
```
##  Mes Comptes & Informations Auteur

* **Auteur / Analyste BI :** `[Mohamed BEN ALI]`
* **Établissement / Formation :** `[CMC-RSK / Module : Concevoir un dashboard]`
* **Email :** [Mohamed BEN ALI](mohammedbenali4321@gmail.com)
* **Roadmap :** [Mohamed BEN ALI](https://roadmap.sh/u/benalimohamed)
* **Kaggle :** [mbaitri](https://www.kaggle.com/mbaitri)
* **LinkedIn :** [Mohamed BEN ALI](https://www.linkedin.com/in/mohamed-ben-ali-m/)
* **Power BI Service / Portfolio :** [???]
  
---

##  Prérequis et Utilisation
1. Ouvrir le fichier `AtlasDistrib_NomPrenom.pbix` avec **Power BI Desktop**.
2. Mettre à jour le paramètre **`DossierDonnees`** dans Power Query (`Accueil > Gérer les paramètres`) avec le chemin local contenant le dossier des sources de données (terminé par `\`).
3. Cliquer sur **Actualiser** pour exécuter automatiquement toutes les étapes de nettoyage et mettre à jour les visuels.
