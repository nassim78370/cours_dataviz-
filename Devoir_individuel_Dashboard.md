#  FORTNITE — ARSENAL ANALYTICS

Dashboard interactif réalisé avec **Python, Streamlit et Pandas**
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

<img width="1919" height="1031" alt="Capture d&#39;écran 2026-10-22 210602" src="https://github.com/user-attachments/assets/e8229365-f43c-4b34-a453-f0beb041d8e4" />

<img width="1919" height="552" alt="Capture d&#39;écran 2026-10-22 210632" src="https://github.com/user-attachments/assets/54a357c3-8d85-4ada-a66f-acbd25ba59bc" />

---

## Choix des couleurs

La palette de couleurs du dashboard a été choisie pour coller à l'univers visuel du jeu Fortnite :

- **Bleu `#1B90DD`** : couleur emblématique de l'interface Fortnite, utilisée comme fond principal
- **Bleu nuit `#0d3060`** : fond des panneaux et graphiques, reprenant les tons sombres des menus du je
u
- **Or `#d9a93a`** : couleur des éléments Légendaires dans le jeu, utilisée pour les titres et accents
- **Couleurs de rareté** : reprises exactement du jeu : gris (Commune), vert (Peu commune), bleu (Rare)
, violet (Épique), or (Légendaire)

Ce choix permet à un joueur de Fortnite de reconnaître immédiatement les niveaux de rareté sans légende
 supplémentaire, tout en offrant unehérente conformément aux bonnes pratiq
ues de visualisation de données.

---

## Technologies utilisées

- **Python 3.12**
- **Streamlit** — interface web interactive
- **Pandas** — traitement des données
- **NumPy** — calcul de la droite de tendance

## Source des données

Jeu de données *Fortnite BR Weapon Attributes* disponible sur [Kaggle](https://www.kaggle.com), 2019.  
43 variantes d'armes · 14 attributs par arme.
