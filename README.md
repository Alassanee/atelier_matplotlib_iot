# Atelier Matplotlib — Visualisation de données IoT

## Contexte

Une entreprise possède plusieurs bâtiments équipés de capteurs IoT. Chaque capteur collecte
régulièrement des informations sur la température, l'humidité, la pression, la consommation
énergétique et l'état du capteur, avec le bâtiment ainsi que la date et l'heure de la mesure.

Cet atelier a pour objectif d'exploiter ces données avec **NumPy**, **Pandas** et **Matplotlib**
afin d'identifier des tendances, des différences entre bâtiments et des anomalies.

## Structure du projet

```
atelier_matplotlib_iot/
│
├── data/
│   └── mesures_capteurs.csv
├── notebooks/
│   └── atelier_matplotlib_iot.ipynb
└── exports/
    ├── temperature.png
    └── temperature.pdf
```

## Prérequis

- Python 3.x
- Jupyter Notebook
- pandas
- matplotlib

## Installation

```bash
git clone <url-du-depot>
cd atelier_matplotlib_iot
pip install pandas matplotlib
jupyter notebook notebooks/atelier_matplotlib_iot.ipynb
```

## Contenu de l'atelier

| Partie | Description |
|--------|-------------|
| 1 | Graphique linéaire — évolution de la température dans le temps |
| 2 | Diagramme en barres — consommation moyenne par bâtiment (vertical et horizontal) |
| 3 | Histogramme — distribution des températures et de la consommation |
| 4 | Nuage de points — relation entre température et consommation |
| 5 | Box plot — dispersion de la température et de la consommation |
| 6 | Diagramme circulaire — répartition des états des capteurs (OK, ALERTE, ERREUR) |
| 7 | Courbes superposées — évolution de la température pour les 4 bâtiments |
| 8 | Sauvegarde des graphiques en PNG et PDF dans `exports/` |
| 9 | Bonus — voir ci-dessous |


## Bonus — Heatmap de corrélation
 
En complément des visualisations demandées, une **heatmap (carte de chaleur) de corrélation**
a été ajoutée pour analyser les liens entre toutes les variables numériques du dataset
(température, humidité, pression, consommation) en une seule vue.
 
Chaque case de la heatmap affiche le coefficient de corrélation (entre -1 et 1) entre deux
variables, avec un code couleur : plus la couleur est intense (rouge ou bleu), plus la relation
entre les deux variables est forte (positive ou négative). Une valeur proche de 0 indique
l'absence de lien linéaire.
 
**Utilité :**
- Elle permet d'identifier en un coup d'œil les variables qui évoluent ensemble (par exemple,
  la température et la consommation énergétique), ce que le nuage de points de la Partie 4
  ne permet de voir que pour une seule paire de variables à la fois.
- Elle aide à repérer d'éventuelles redondances entre variables avant une analyse plus poussée
  ou une modélisation (deux variables très corrélées apportent une information similaire).
- Elle donne une vue d'ensemble rapide et synthétique, utile pour orienter la suite de
  l'exploration des données (quelles paires de variables approfondir en priorité).

<!-- décrire ici la fonctionnalité bonus une fois implémentée -->

## Auteur
### Alassane Mbengue
Réalisé dans le cadre de la formation IA — Orange Digital Center.
