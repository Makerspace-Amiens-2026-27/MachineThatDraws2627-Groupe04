---
layout: default
nav_order: 4
title: Études et choix techniques
---

# Études et choix techniques


## Recherche de l'existant

## Recherche de l'existant et faisabilité

Avant de concevoir notre machine, nous avons étudié un produit du commerce de référence et plusieurs projets DIY (Instructables, Hackaday, Fab Academy) pour comprendre les choix techniques courants et vérifier que notre projet est réalisable dans le délai.

### Tableau de synthèse

| Solution étudiée | Source | Avantages | Inconvénients | Ce qu'on retient |
|---|---|---|---|---|
| AxiDraw (Evil Mad Scientist), traceur du commerce | [Fiche produit](https://shop.evilmadscientist.com/846) · [Article Make:](https://makezine.com/2016/12/05/evil-mad-scientist-labs-release-axidraw-a-writing-and-drawing-machine/) | Livré monté, zone de tracé A4 ou A3, nombreux types de stylos, pilotage depuis Inkscape (logiciel libre) | Prix élevé, mécanique fermée qu'on ne peut pas adapter | Référence pour l'usage (fichier vectoriel → tracé, levée du stylo). On construit notre propre machine. |
| CoreXY CNC Plotter (Arduino Uno + GRBL) | [Instructables](https://www.instructables.com/CoreXY-CNC-Plotter) | Code fourni, très documenté, pièces imprimées en 3D | Cinématique CoreXY plus délicate à régler, pas d'écran ni d'arrêt d'urgence | On reprend GRBL et le servo pour le stylo. On écarte le CoreXY. |
| CNC Plotter avec GRBL-Servo et pen-lift | [Instructables](https://www.instructables.com/CNC-Plotter-1) | Levée du stylo par servo intégrée à GRBL, envoi du G-code avec UGS | Réglages GRBL à faire avec soin | Piste pour le firmware et l'envoi du G-code. À confirmer par un test. |
| Pen plotter CoreXY (Pilvi), Fab Academy Aalto | [Fab Academy 2022](https://fabacademy.org/2022/labs/aalto/students/matti-niinimaki/weekly-assignments/week11) | Montage et configuration bien détaillés | Réglages de firmware spécifiques au CoreXY | On retient la méthode de configuration de GRBL. |
| The $50 pen plotter (moteurs 28BYJ-48) | [Hackaday, mars 2023](https://hackaday.com/2023/03/19/the-50-pen-plotter) | Très peu coûteux | Moteurs peu puissants, précision limitée | Écarté : nos moteurs pas à pas sont plus puissants. |
| Pen plotter CoreXY avec firmware Zephyr | [Hackaday.io](https://hackaday.io/project/177237/log/198574) | Conception complète, firmware sur mesure | Développer un firmware prend trop de temps | Écarté. Idée d'évolution seulement. |
| *Projets du MakerSpace des années précédentes* | *À compléter* | | | |

### Notre choix : une machine cartésienne

La plupart des projets étudiés utilisent une cinématique **CoreXY** (deux moteurs fixes et des courroies croisées). Nous avons choisi une machine **cartésienne**, où chaque axe a son propre moteur et son propre guidage.

| | Cartésienne (notre choix) | CoreXY |
|---|---|---|
| Principe | Un moteur par axe (X et Y indépendants) | Les deux moteurs agissent ensemble sur chaque mouvement |
| Réglage de GRBL | Standard, sans option particulière | Mode CoreXY à activer, sens des moteurs à vérifier |
| Mise au point | Simple : on teste chaque axe séparément | Plus délicate : une erreur de courroie ou de sens décale tout le tracé |
| Pièces | Courroies et guidages simples | Croisement des courroies, plus de poulies |

Ce choix réduit le risque de réglage et facilite le dépannage, ce qui compte pour un projet au délai court.

### Faisabilité

| Critère | Évaluation |
|---|---|
| Mécanique | Réalisable : tiges de guidage, courroies, pièces imprimées en 3D, profilés aluminium |
| Électronique | Réalisable : carte de commande, drivers, fins de course, arrêt d'urgence, écran OLED |
| Logiciel | Réalisable : GRBL et un logiciel d'envoi de G-code existent déjà |
| Risque principal | Calibrage fin et levée du stylo : prévoir du temps pour les essais |

### Conclusion

Nous reprenons les briques éprouvées (GRBL, levée du stylo par servo, pilotage par G-code) avec une mécanique cartésienne plus simple à régler. Nous ajoutons la sécurité et l'autonomie (arrêt d'urgence, fins de course, écran). Le changement automatique de couleur de stylo reste une piste pour une version 2.

### Sources

- Evil Mad Scientist, [AxiDraw V3](https://shop.evilmadscientist.com/846)
- Make:, [AxiDraw V3](https://makezine.com/2016/12/05/evil-mad-scientist-labs-release-axidraw-a-writing-and-drawing-machine/)
- Instructables, [CoreXY CNC Plotter](https://www.instructables.com/CoreXY-CNC-Plotter)
- Instructables, [CNC Plotter](https://www.instructables.com/CNC-Plotter-1)
- Fab Academy Aalto 2022, [Pen Plotter Using CoreXY](https://fabacademy.org/2022/labs/aalto/students/matti-niinimaki/weekly-assignments/week11)
- Hackaday, [The $50 pen plotter](https://hackaday.com/2023/03/19/the-50-pen-plotter)
- Hackaday.io, [CoreXY pen plotter](https://hackaday.io/project/177237/log/198574)
## Pré-étude de faisabilité

{: .a_modifier }
> Quels points techniques vous inquiétaient, et comment les avez-vous testés
> rapidement (montage sur platine d'essai, pièce imprimée de test…) ? Résultats ?
> Vous pouvez résumer ici et détailler les protocoles et mesures dans la page
> [Tests et résultats](tests.md), avec un lien vers la section concernée.

Exemple : test du capteur de couleur sous l'éclairage réel sur 30 déchets :
27 correctement identifiés.

## Choix techniques retenus

Architecture cartésienne
-Axes X et Y indépendants.
-Conception simple.
-Bonne précision.
-Maintenance facilitée.

Moteurs pas à pas NEMA 17
-Déplacement précis.
-Fiabilité élevée.
-Faciles à piloter.
-Largement utilisés dans les CNC et imprimantes 3D.

Courroies GT2 et poulies dentées
-Déplacements fluides.
-Bonne précision.
-Mise en œuvre simple.
-Technologie éprouvée.

ESP32
-Puissance de calcul élevée.
-Wi‑Fi intégré.
-Mémoire importante.
-Possibilités d'évolution futures.

Support de maintien de la feuille
-Maintien efficace de la feuille.
-Réduction des déplacements du papier.
-Amélioration de la qualité du tracé.

Levage du stylo par servomoteur
-Faible encombrement.
-Commande simple.
-Mouvement précis.
-Adapté au levage du stylo

### Choix : Machine cartésienne

**Contexte :** …

**Options envisagées :** …

**Choix retenu et pourquoi :** …

**Compromis acceptés :** …
