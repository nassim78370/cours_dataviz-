# Lisibilité des visualisations et accidents corporels en Île-de-France (2025)

## Partie 1 – Les règles de lisibilité 7 à 16

**Règle 7 – Étiquettes et graduations lisibles.** Dans l'exemple, les six longues étiquettes de l'axe horizontal se chevauchent et deviennent illisibles. La correction consiste à incliner les étiquettes, qui restent alors lisibles. Si elles ne rentrent toujours pas, il vaut mieux raccourcir les libellés ou simplifier le graphique plutôt que de multiplier les rotations.

**Règle 8 – Accessibilité des couleurs.** Le graphique en anneau utilise six couleurs et une légende : certaines teintes sont proches et la couleur seule ne suffit pas à distinguer les catégories (daltonisme, impression en noir et blanc). L'exemple corrigé ajoute des étiquettes directes et des motifs (hachures, points, quadrillage) qui apportent des indices en plus de la couleur.

**Règle 9 – Étiquetage direct.** Dans l'exemple, une légende de quatre lignes oblige le lecteur à faire des allers-retours entre la légende et les courbes. La correction est d'écrire le nom de chaque courbe directement à son extrémité, ce qui fonctionne bien quand il n'y a que deux à quatre séries.

**Règle 10 – Éviter le chartjunk.** La courbe de l'exemple est noyée dans une grille dense, sans étiquettes, qui n'apporte aucune information. La version corrigée garde peu de lignes de grille, légères, et la courbe ressort : chaque élément visible doit aider à lire une comparaison.

**Règle 11 – Trop de catégories.** Avec 15 catégories, le graphique à barres est difficile à parcourir et la comparaison se transforme en lecture d'étiquettes. L'exemple corrigé ne garde que les 6 catégories principales ; on peut aussi agréger ou faire des facettes.

**Règle 12 – Trier les barres.** Les barres A, B, C, D ne sont pas triées, ce qui ralentit la comparaison et cache les extrêmes. La correction trie par valeur décroissante (A, C, D, B), sauf quand les catégories ont un ordre naturel (mois, âges…).

**Règle 13 – Surimpression dans les nuages de points.** Dans l'exemple, les marqueurs de même taille cachent les observations répétées : plusieurs points sont superposés et on ne voit pas combien. La version corrigée fait varier la taille de la bulle selon le nombre d'observations. D'autres solutions existent : transparence, jitter, hexagones, agrégation.

**Règle 14 – Précision décimale.** Les graduations de l'axe horizontal (0.1111, 0.2222, 0.3333) donnent une précision inutile qui ralentit la lecture. La correction arrondit à deux décimales (0.11, 0.22, 0.33) : la précision doit correspondre à la décision, pas à la sortie brute de la machine.

**Règle 15 – Formatage des dates.** Les dates complètes (2026-01-02, 2026-01-03…) se chevauchent sur l'axe. La version corrigée affiche moins de graduations et un format court (« Jan 1 », « Jan 4 », « Jan 8 »). On commence par réduire le nombre de graduations, puis on raccourcit le format, et on ne tourne les étiquettes qu'en dernier recours.

**Règle 16 – Économie visuelle.** Avec 80 barres, le graphique est surchargé et les étiquettes sont illisibles. L'exemple corrigé ne montre que les 10 principaux comptes : montrer tout en même temps dilue le message, et la simplification est souvent la meilleure refonte.

---

## Partie 2 – Cartographie des accidents en Île-de-France

**Données et nettoyage.** J'ai utilisé le fichier `caract-2025.csv` (data.gouv.fr, ONISR) : 55 093 accidents corporels en France, outre-mer compris. Je n'ai gardé que les 8 départements d'Île-de-France, soit **14 760 accidents**. Nettoyage : coordonnées converties (virgule décimale, espaces parasites), valeur manquante `-1` remplacée, et contrôle que chaque point tombe dans son département (aucune erreur). Variables utilisées : `lat`/`long`, `dep` et `hrmn` (heure). Le code est dans `analyse_accidents_idf.py`.

![Les trois graphiques](images/synthese_3_graphiques.png)

**Carte (à gauche).** Chaque hexagone est coloré selon la densité d'accidents : plus il est foncé, plus il y a d'accidents. Le maximum se trouve au cœur de Paris (jusqu'à 442 accidents dans un hexagone), et la densité décroît avec la distance au centre. Les grands axes routiers apparaissent comme des traînées d'hexagones qui rayonnent depuis Paris jusqu'en grande couronne.

**Accidents par heure (en haut à droite).** Le nombre d'accidents est minimal la nuit (158 à 3 h) et présente deux pics : le matin (1 019 à 8 h) et surtout en fin d'après-midi, avec un maximum de 1 170 à 18 h, mis en évidence par la barre foncée. Ces pics correspondent aux trajets domicile-travail. Entre 10 h et 15 h, le nombre reste stable autour de 650 à 750 par heure.

**Accidents par département (en bas à droite).** Paris est en tête avec 3 681 accidents (25 % de la région), suivi de la Seine-Saint-Denis (2 355), des Hauts-de-Seine (2 289) et du Val-de-Marne (2 017). Les départements de grande couronne ont moins d'accidents (de 860 pour le Val-d'Oise à 1 338 pour l'Essonne). Paris et la petite couronne concentrent 70 % des accidents, ce qui confirme la carte.

**Limites.** Ce sont des effectifs, pas des taux : sans trafic ni population, on ne peut pas dire qu'un département est « plus dangereux ». Le fichier ne contient pas non plus la gravité (blessés, tués).

### Règles de lisibilité appliquées

- **Règle 7 – Étiquettes et graduations :** une graduation sur deux pour les heures, et barres horizontales pour les noms de départements.
- **Règle 8 – Couleurs :** une seule teinte (rouge) en intensité variable ; les départements sont nommés, donc la couleur n'est pas le seul indice.
- **Règle 9 – Étiquetage direct :** départements nommés sur la carte, valeurs au bout des barres, pas de légende.
- **Règle 10 – Chartjunk :** pas de cadre, carte sans axes, grille horizontale très claire.
- **Règle 12 – Tri des barres :** départements triés par ordre décroissant.
- **Règle 13 – Surimpression :** hexagones colorés à la place de 14 760 points opaques (voir ci-dessous).
- **Règle 14 – Précision décimale :** effectifs en nombres entiers.
- **Règle 16 – Économie visuelle :** une information par graphique, un seul accent de couleur.

Contre-exemple pour la règle 13 : le nuage de points direct est illisible au centre.

![Nuage de points direct](images/fig0_contre_exemple_nuage_points.png)

### Justification des choix

- **Hexagones** : ils gardent la structure géographique et les différences de densité que les points masquent.
- **Rouge** : un dégradé d'une seule teinte se lit facilement, et le rouge évoque un phénomène négatif. La barre de couleur indique seulement « Faible » et « Forte » : le nombre exact par hexagone n'intéresse pas le lecteur.
- **Barres pour les heures** : on compte des accidents par heure, ce que des barres représentent mieux qu'une courbe, qui suggère une continuité.
- **Barres horizontales triées pour les départements** : les noms sont longs et il n'y a pas d'ordre naturel.

Pour reproduire : placer `caract-2025.csv` et `departements.geojson` dans `data/`, puis `python analyse_accidents_idf.py`.
