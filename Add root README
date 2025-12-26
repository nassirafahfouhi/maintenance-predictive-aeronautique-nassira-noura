# Maintenance Prédictive Aéronautique par IA (NASA C-MAPSS)

Projet universitaire réalisé par **Nassira FAHFOUHI** et **Noura KAZDARI** dans le cadre du module *Maintenance Prédictive Aéronautique par Intelligence Artificielle* (ENSA Safi – Département GINF / GATE3).

## Objectif

Développer un modèle de Machine Learning capable d’estimer la **Remaining Useful Life (RUL)** de turboréacteurs à partir du jeu de données **NASA C-MAPSS – sous-ensemble FD001**.

## Contenu du dépôt

- `Data/train_FD001.txt` : historique complet de 100 moteurs jusqu’à la panne.  
- `Data/test_FD001.txt` : 100 autres moteurs observés jusqu’à un certain cycle.  
- `Data/RUL_FD001.txt` : RUL vraie pour les moteurs du jeu de test.  
- `Data/Untitled.ipynb` : notebook Jupyter contenant  
  - chargement et description du dataset,  
  - calcul de la RUL pour chaque cycle,  
  - nettoyage des features (suppression capteurs constants),  
  - normalisation Min-Max,  
  - entraînement et évaluation des modèles (Régression Linéaire & Random Forest),  
  - courbes **RUL vraie vs prédite** pour plusieurs moteurs.  
- `Maintenance Prédictive Aéronautique par Intelligence Artificielle Nassira & Noura.pdf` : rapport technique complet du projet.

## Méthodologie ML

1. **Prétraitement**
   - Calcul de la RUL : \( RUL = \text{cycle\_max\_moteur} - \text{cycle\_actuel} \).  
   - Suppression de `engine_id`, `cycle` et des capteurs quasi constants.  
   - Normalisation Min-Max des capteurs retenus.

2. **Modèles testés**
   - Baseline : **Régression Linéaire**.  
   - Modèle avancé : **RandomForestRegressor** (scikit-learn).

3. **Métrique**
   - **RMSE** (Root Mean Square Error) sur le jeu de test FD001.

## Résultats principaux

- Erreur moyenne RUL ≈ **41 cycles** (≈10 % d’erreur relative).  
- Les capteurs les plus importants pour la prédiction sont notamment `s11`, `s4` et `s9`.  
- Le modèle est acceptable pour un démonstrateur académique, mais non directement certifiable pour une intégration avion réelle (données synthétiques, pas de DO-178C / DO-254).

## Remarques

Ce projet a pour but pédagogique de montrer une chaîne complète de **maintenance prédictive par IA** (de la donnée brute NASA à la prédiction de RUL) dans un contexte aéronautique (Airbus, Boeing, Safran, GE).
