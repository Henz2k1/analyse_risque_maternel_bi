::: {align="center"}
# Analyse du risque maternel avec Power BI

### Projet personnel · Data Analytics & Business Intelligence

[![Power
BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Python](https://img.shields.io/badge/Python-Data%20Preparation-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Status](https://img.shields.io/badge/Status-Completed-2E8B57?style=for-the-badge)]()

**De la préparation des données à la visualisation interactive.**
:::

------------------------------------------------------------------------

## Aperçu du tableau de bord

Le rapport Power BI propose une vue synthétique des niveaux de risque
maternel et des principaux indicateurs physiologiques observés dans le
jeu de données.

```{=html}
<p align="center">
```
`<img src="captures/dashboard_risque_maternel.png" alt="Tableau de bord Power BI - Analyse du risque maternel" width="100%">`{=html}
```{=html}
</p>
```

------------------------------------------------------------------------

## 1. À propos du projet

Ce projet personnel porte sur l'exploration et la visualisation de
données relatives au risque maternel chez les femmes enceintes.

Après une première étape de préparation et de nettoyage des données avec
Python, **Microsoft Power BI** est utilisé pour construire un tableau de
bord interactif. Celui-ci facilite la lecture des données, la
comparaison des catégories de risque et l'exploration des relations
entre plusieurs indicateurs physiologiques.

### Problématique

> Comment la visualisation interactive peut-elle faciliter la
> compréhension de la répartition des niveaux de risque maternel et des
> facteurs qui leur sont associés dans les données ?

### Objectifs

-   Présenter la répartition des patientes selon leur niveau de risque.
-   Synthétiser les principaux indicateurs à l'aide de KPI.
-   Comparer les niveaux de risque selon les classes de glycémie.
-   Explorer la relation entre glycémie et pression artérielle
    systolique.
-   Permettre une exploration dynamique à l'aide de filtres.

------------------------------------------------------------------------

## 2. Données utilisées

Les données proviennent du jeu **Fighting Maternal Risk**, disponible
sur Kaggle.

  ------------------------------------------------------------------------------------------------------
  Information                         Détail
  ----------------------------------- ------------------------------------------------------------------
  Source                              [Kaggle -- Fighting Maternal
                                      Risk](https://www.kaggle.com/competitions/mlolympiadbd2025/data)

  Fichier principal                   `train_clean.csv`

  Observations analysées              809

  Origine indiquée du jeu             Bangladesh
  ------------------------------------------------------------------------------------------------------

### Variables principales

  Variable         Description                       Unité
  ---------------- --------------------------------- --------------
  `Age`            Âge de la femme enceinte          Années
  `SystolicBP`     Pression artérielle systolique    mmHg
  `DiastolicBP`    Pression artérielle diastolique   mmHg
  `BloodGlucose`   Glycémie                          mmol/L
  `BodyTemp_C`     Température corporelle            °C
  `HeartRate`      Fréquence cardiaque               bpm
  `RiskLabel`      Catégorie de risque maternel      Catégorielle

### Catégories de risque

-   🟢 **Low Risk** --- risque faible
-   🟡 **Mid Risk** --- risque modéré
-   🟣 **High Risk** --- risque élevé

------------------------------------------------------------------------

## 3. Tableau de bord et indicateurs

Le rapport, intitulé **Analyse Risque Maternel -- Dashboard**, rassemble
plusieurs visualisations complémentaires.

### KPI principaux

  Indicateur                       Valeur affichée
  ------------------------------ -----------------
  Nombre total de patientes                **809**
  Patientes de moins de 18 ans         **18,67 %**
  Pression systolique moyenne      **113,09 mmHg**
  Glycémie moyenne                 **8,66 mmol/L**

### Visualisations

  -----------------------------------------------------------------------
  Visualisation                       Utilité
  ----------------------------------- -----------------------------------
  Colonnes empilées à 100 %           Comparer la répartition des risques
                                      par classe de glycémie

  Nuage de points                     Explorer la relation entre glycémie
                                      et pression systolique, avec
                                      distinction par niveau de risque

  Diagramme circulaire                Visualiser la répartition des
                                      patientes selon `RiskLabel`

  Jauge                               Mettre en évidence le nombre de
                                      patientes classées à risque élevé
  -----------------------------------------------------------------------

### Répartition observée

  Niveau de risque     Effectif        Part
  ------------------ ---------- -----------
  Low Risk                  323     39,93 %
  Mid Risk                  269     33,25 %
  High Risk                 217     26,82 %
  **Total**             **809**   **100 %**

### Interactivité

Le tableau de bord comprend des filtres permettant d'explorer les
données selon :

-   la tranche d'âge ;
-   le niveau de risque.

Les interactions entre les visuels permettent d'affiner l'analyse en
fonction des sélections effectuées.

------------------------------------------------------------------------

## 4. Principaux constats descriptifs

Les visualisations mettent notamment en évidence les éléments suivants :

-   Les observations sont réparties entre trois catégories de risque,
    avec une part de **26,82 %** classée High Risk.
-   La glycémie moyenne affichée est de **8,66 mmol/L**.
-   La pression systolique moyenne affichée est de **113,09 mmHg**.
-   Les classes de glycémie les plus élevées présentent une proportion
    importante de patientes classées à risque élevé dans ce jeu de
    données.

Ces constats décrivent les observations disponibles. Ils ne démontrent
pas de causalité et ne constituent pas des conclusions ou
recommandations médicales.

------------------------------------------------------------------------

## 5. Technologies utilisées

  -----------------------------------------------------------------------
  Outil                               Rôle dans le projet
  ----------------------------------- -----------------------------------
  **Microsoft Power BI Desktop**      Création du rapport et des
                                      visualisations

  **Power Query**                     Importation et préparation des
                                      données dans Power BI

  **DAX**                             Création des mesures et indicateurs

  **Python / Pandas**                 Exploration et nettoyage préalables
                                      des données

  **Git / GitHub**                    Versionnement et partage du projet
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 6. Structure du dépôt

``` text
analyse-risque-maternel-powerbi/
│
├── README.md
│
├── donnees/
│   └── train_clean.csv
│
├── powerbi/
│   └── analyse_risque_maternel.pbix
│
└── captures/
    └── dashboard_risque_maternel.png
```

*Adapte cette arborescence aux noms et aux emplacements réellement
utilisés dans ton dépôt. Le fichier de données peut être omis du dépôt
si sa redistribution n'est pas autorisée.*

------------------------------------------------------------------------

## 7. Utilisation du rapport

### Prérequis

-   Windows ;
-   Microsoft Power BI Desktop ;
-   le fichier de rapport `.pbix` ;
-   le fichier de données source, si celui-ci n'est pas intégré au
    modèle.

### Ouvrir le projet

1.  Cloner ou télécharger le dépôt GitHub.
2.  Ouvrir le fichier `.pbix` avec Power BI Desktop.
3.  Si Power BI signale une source introuvable, mettre à jour le chemin
    du fichier CSV dans les paramètres de source ou dans Power Query.
4.  Actualiser les données.
5.  Utiliser les filtres et les interactions pour explorer le rapport.

------------------------------------------------------------------------

## 8. Limites et précautions d'interprétation

-   Le jeu de données provient du Bangladesh ; les résultats ne sont pas
    automatiquement généralisables à d'autres populations.
-   Les variables disponibles ne couvrent pas tous les facteurs
    susceptibles d'être associés au risque maternel.
-   Les visualisations décrivent des associations et des distributions,
    sans établir de relation de cause à effet.
-   Les catégories de risque et les seuils présents dans le jeu doivent
    être interprétés selon la documentation de la source.
-   Ce tableau de bord est un exercice d'analyse de données et ne
    constitue pas un outil de diagnostic médical.

------------------------------------------------------------------------

## 9. Pistes d'amélioration

-   Ajouter des pages d'analyse dédiées à chaque dimension du risque
    maternel.
-   Enrichir les info-bulles et les interactions.
-   Documenter les mesures DAX et les règles de calcul des KPI.
-   Intégrer des variables supplémentaires si des données fiables sont
    disponibles.
-   Approfondir l'analyse statistique dans un travail complémentaire.

------------------------------------------------------------------------

## 10. À propos

**Projet personnel --- Data Analytics & Business Intelligence**

Ce projet illustre une démarche allant de la préparation des données
avec Python à leur exploration visuelle avec Power BI.

Il a pour objectif de mettre en pratique des compétences en préparation,
analyse, modélisation et visualisation des données.

------------------------------------------------------------------------

::: {align="center"}
**Analyse · Compréhension · Visualisation**

*Transformer les données en informations lisibles et explorables.*
:::
