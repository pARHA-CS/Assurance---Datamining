# Assurance - DataMining

## Description du projet

Ce projet universitaire consiste à appliquer des techniques de datamining pour sélectionner le meilleur modèle prédictif permettant de déterminer si un client de l'assurance santé souscrira également une assurance automobile auprès de la même compagnie. L'objectif est d'explorer, comparer et évaluer différents modèles pour obtenir des prédictions fiables et exploitables.

## Objectifs

- Utiliser des méthodes de datamining pour la prédiction.
- Comparer les performances de plusieurs modèles prédictifs.
- Fournir des recommandations sur le modèle le plus performant en fonction des métriques sélectionnées.

## Technologies utilisées

- **Langage principal** : R
- Outils et bibliothèques spécifiques (`tidymodels`, `pROC`, `caret`, `xgboost`, `xgboost`,).

Voici la mise à jour de la section **Contenu du projet** intégrant la partie sur le rééquilibrage des données :

---

## Contenu du projet

Le projet comprend les éléments suivants :

1. **Exploration des données** :  
   Analyse descriptive des données, visualisations, et gestion des données manquantes.

2. **Prétraitement des données** :  
   - Normalisation et codage des variables catégoriques.  
   - Rééquilibrage des classes pour corriger un déséquilibre significatif entre les réponses "Oui" et "Non". Les techniques suivantes ont été utilisées :  
     - **Sur-échantillonnage** des observations minoritaires.  
     - **Sous-échantillonnage** des observations majoritaires.  
     - (Optionnel) Application de **SMOTE** pour générer des exemples synthétiques, selon les besoins.  

   Cette étape a permis de créer une base de données équilibrée et adaptée à une évaluation équitable des modèles prédictifs.

3. **Implémentation des modèles** :  
   - Régression logistique  
   - Arbres de décision  
   - Random Forest  
   - SVM (Support Vector Machines)  
   - (Autres modèles si applicable)  

4. **Évaluation des modèles** :  
   - Métriques utilisées : précision, rappel, F1-score, AUC-ROC.  
   - Validation croisée pour évaluer la robustesse des modèles.  

5. **Recommandations** :  
   Sélection du modèle le plus performant et analyse de ses résultats.  

---

Cette version explique clairement où et comment le rééquilibrage des données s'inscrit dans le projet. 😊

## Prérequis

- **Logiciels** :
  - R version 3.2 ou supérieure
  - RStudio (optionnel, mais recommandé)
- **Packages R nécessaires** (installer avec `install.packages()`) :
 Voici la version mise à jour de la section **Prérequis** avec l'inclusion des librairies nécessaires directement dans le texte :

---

## Prérequis

- **Logiciels** :
  - R version 4.x ou supérieure
  - RStudio (optionnel, mais recommandé)

- **Packages R nécessaires** (installer avec `install.packages()` ou `remotes::install_github()` pour certains) :

```R
install.packages(c("tidymodels", "tidyverse", "workflows", "tune", "doParallel", 
                   "kableExtra", "pROC", "discrim", "dplyr", "caret", "xgboost", 
                   "knitr", "modelsummary", "vip", "ggdark", "showtext", 
                   "ggplot2", "palmerpenguins", "xtable"))
```

Ces packages sont utilisés pour diverses étapes du projet, telles que :

- **`tidymodels`** et **`workflows`** : pour la gestion des modèles prédictifs et la création de workflows.
- **`tune`** : pour la sélection et l'ajustement des hyperparamètres des modèles.
- **`doParallel`** : pour paralléliser les tâches et accélérer les traitements.
- **`kableExtra`** et **`knitr`** : pour la génération de rapports dynamiques avec des tables bien formatées.
- **`pROC`** : pour l'analyse des performances des modèles à l'aide de courbes ROC et de l'AUC.
- **`discrim`** : pour l'implémentation de l'analyse discriminante.
- **`dplyr`** et **`tidyverse`** : pour la manipulation, nettoyage et transformation des données.
- **`caret`** : pour l'entraînement des modèles et la validation croisée.
- **`xgboost`** : pour les modèles de boosting, notamment pour des prédictions de haute performance.
- **`modelsummary`** : pour résumer et afficher les résultats des modèles.
- **`vip`** : pour visualiser l'importance des variables dans les modèles.
- **`ggdark`**, **`showtext`**, et **`ggplot2`** : pour créer des visualisations graphiques personnalisées.
- **`palmerpenguins`** : pour utiliser des jeux de données d'exemple, tels que ceux sur les manchots.
- **`xtable`** : pour générer des tables en LaTeX ou HTML dans les rapports.


## Installation

1. Cloner le dépôt ou télécharger les fichiers du projet :
   ```bash
   git clone https://github.com/pARHA-CS/Assurance-Datamining.git
   ```
2. Ouvrir le projet dans RStudio.
3. Installer les packages requis :
  ```R
install.packages(c("tidymodels", "tidyverse", "workflows", "tune", "doParallel", 
                   "kableExtra", "pROC", "discrim", "dplyr", "caret", "xgboost", 
                   "knitr", "modelsummary", "vip", "ggdark", "showtext", 
                   "ggplot2", "palmerpenguins", "xtable"))
```

## Utilisation

1. Charger les données d'assurance fournies (`train.csv`, `resampled_data_new.csv`, `resampled_data_new_10k.csv`).
2. Exécuter le script.
3. Consulter les résultats finaux dans le fichier généré (`rapport_final.pdf` ou autre).

## Résultats attendus

- Un rapport détaillant les performances des modèles testés.
- Une recommandation claire sur le modèle prédictif optimal.

## Auteurs

- Raphaël Mercier
- Alexis Savaton
