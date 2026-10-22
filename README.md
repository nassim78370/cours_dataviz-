# 🎯 FORTNITE — ARSENAL ANALYTICS

Dashboard interactif réalisé avec **Python, Streamlit, Pandas et Plotly Express**
sur les caractéristiques des armes de Fortnite Battle Royale (jeu de données
*Fortnite BR Weapon Attributes*, Kaggle, 2019 : 43 variantes d'armes).

---

## Description du projet

Ce dashboard analyse les performances des armes du jeu **Fortnite Battle Royale** à partir d'un jeu de données recensant 43 variantes d'armes réparties en 6 catégories (fusils d'assaut, fusils de précision, fusils à pompe, pistolets-mitrailleurs, pistolets, explosifs) et 5 niveaux de rareté (Commune, Peu commune, Rare, Épique, Légendaire).

L'objectif est de visualiser les différences de performances entre les catégories et les raretés d'armes, en s'appuyant sur les variables clés : **DPS** (dégâts par seconde), **dégâts par tir**, **cadence de tir** et **taille du chargeur**.

---

## Visualisations

| Graphique | Type | Description |
|---|---|---|
| Répartition par rareté | Graphique circulaire | Proportion des armes selon leur niveau de rareté |
| DPS moyen par catégorie | Barres horizontales | Comparaison des dégâts par seconde moyens entre les 6 catégories d'armes |
| Top 10 dégâts par tir | Barres horizontales | Classement des 10 armes infligeant le plus de dégâts en un seul tir |
| Dégâts vs Cadence | Nuage de points | Corrélation entre les dégâts par tir et la cadence de tir, avec droite de tendance |
| Distribution du DPS | Boîte à moustaches | Distribution statistique des dégâts par seconde par catégorie d'armes |

---

## Captures d'écran

![Dashboard - partie haute](<Capture d'écran 2026-10-22 210602.png>)

![Dashboard - partie basse](<Capture d'écran 2026-10-22 210632.png>)

---

## Technologies utilisées

- **Python 3.12**
- **Streamlit** — interface web interactive
- **Plotly Express** — visualisations interactives
- **Pandas** — traitement des données
- **NumPy** — calcul de la droite de tendance

## Source des données

Jeu de données *Fortnite BR Weapon Attributes* disponible sur [Kaggle](https://www.kaggle.com), 2019.  
43 variantes d'armes · 14 attributs par arme.
