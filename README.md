# TP N°1 : Classification de Clients avec Random Forest 🌌

[![Algorithme](https://img.shields.io/badge/Algorithme-Random_Forest-00e5ff.svg)](#)
[![Thème](https://img.shields.io/badge/Thème-Astronomic_Violet_Blue-8a2be2.svg)](#)
[![Langage](https://img.shields.io/badge/Langage-Python-3776ab.svg)](#)

## 📌 Présentation du Projet

[cite_start]Ce projet porte sur la **classification supervisée des clients** d'un centre commercial afin d'optimiser les stratégies marketing d'une entreprise[cite: 1, 3]. [cite_start]L'objectif est de prédire la catégorie de revenus d'un client en fonction de ses caractéristiques démographiques et comportementales[cite: 200].

Le rendu est présenté sous la forme d'un **compte rendu interactif monolithique (HTML/CSS/JS)** au design "Astronomic Violet Blue", intégrant des visualisations dynamiques et une analyse théorique approfondie.

### 👥 Équipe de Réalisation
* **Auteurs :** Dahane Ahmed Lamine & Tabbi Meriem
* **Enseignante :** Mme. Fergani
* **Module :** Intelligence Artificielle

---

## 🧠 Notions Fondamentales

### L'Algorithme Random Forest
[cite_start]Le Random Forest est un algorithme d'**Ensemble Learning** [cite: 11] [cite_start]basé sur la méthode du **Bagging** (Bootstrap Aggregating)[cite: 16, 46]:
* [cite_start]**Arbres de Décision :** Il construit une forêt de multiples arbres de décision indépendants[cite: 105, 106].
* [cite_start]**Bootstrap :** Chaque arbre est entraîné sur un échantillon aléatoire des données[cite: 108, 132].
* [cite_start]**Aléatoire des variables :** À chaque nœud, un sous-ensemble aléatoire de variables est sélectionné pour la division[cite: 109, 143].
* [cite_start]**Agrégation :** La prédiction finale est obtenue par vote majoritaire pour la classification[cite: 111, 153].

### [cite_start]Avantages et Limites [cite: 156, 177]
* [cite_start]**Avantages :** Très performant et robuste, réduit considérablement le surapprentissage (overfitting) et gère efficacement les grandes quantités de données[cite: 157, 158, 159].
* [cite_start]**Limites :** Moins interprétable qu'un arbre unique (effet boîte noire) et peut être plus lent et gourmand en mémoire avec un grand nombre d'estimateurs[cite: 178, 180, 181].

---

## 📊 Analyse des Données (Dataset)

[cite_start]Le projet utilise le **Mall Customers Dataset**[cite: 5, 198]:
* [cite_start]**Contenu :** 200 enregistrements et 5 variables (`CustomerID`, `Gender`, `Age`, `Annual Income`, `Spending Score`)[cite: 202, 204].
* **Pré-traitement (Nettoyage) :** * **Suppression de l'ID :** La colonne `CustomerID` est retirée car elle ne contient aucune information prédictive et risquerait de bruiter l'apprentissage.
    * **Suppression de la Cible :** La colonne de revenus est extraite pour devenir la variable `y` (target) et doit impérativement être supprimée des variables `X` (features) pour éviter tout biais ("triche" du modèle).
* [cite_start]**Labellisation :** Création de 3 classes de revenus (Faible, Moyen, Élevé) pour permettre l'apprentissage supervisé sur un jeu de données initialement non labellisé[cite: 8, 9].

---

## 📈 Évaluation et Métriques

Le modèle est évalué via plusieurs indicateurs clés :
1.  **Matrice de Confusion :** Un tableau croisant les classes réelles et les prédictions pour identifier précisément les types d'erreurs commises.
2.  **Précision :** Capacité du modèle à ne pas classer à tort un client dans une catégorie (réduction des faux positifs).
3.  **Rapport de Classification :** Résumé incluant la précision, le rappel (recall) et le score F1 pour chaque classe de clients.

---

## 🚀 Utilisation

1.  **Installation :** Clonez le dépôt et assurez-vous d'avoir le fichier `Mall_Customers.csv` dans le dossier.
2.  **Exécution Web :** Ouvrez simplement le fichier `tp1_random_forest.html` dans un navigateur pour consulter le rapport complet et les visualisations interactives.
3.  **Visualisations :** Le rapport inclut des graphiques interactifs (Plotly.js) pour l'**importance des variables** et la **matrice de confusion**.

---

## 📝 Conclusion

[cite_start]Ce TP a permis de démontrer la puissance du **Random Forest** pour la segmentation de clientèle[cite: 186]. Avec une exactitude d'environ **86%**, le modèle prouve que le score de dépense et l'âge sont des indicateurs majeurs du niveau de revenu. Cette approche permet aux entreprises de personnaliser leurs offres de manière proactive et automatisée.

---
*Projet universitaire - 2026*
