---
layout: default
nav_order: 4
title: Études et choix techniques
---

# Études et choix techniques



## Recherche de l'existant

{: .a_modifier }
> Projets du MakerSpace des années précédentes, projets en ligne (Hackaday,
> Instructables, GitHub…), produits du commerce : qu'est-ce qui fait déjà quelque
> chose de proche, et qu'est-ce que vous en retenez ? Citez vos sources.
> Voir [Rechercher l'existant et étudier la faisabilité](https://doc.makerspace-amiens.fr/workshops/methodologie-de-projet/concepts/rechercher-existant-faisabilite/).

| Solution étudiée | Source | Avantages | Inconvénients | Ce qu'on retient |
|---|---|---|---|---|
| Capteur de couleur TCS3200 | Projet Hackaday similaire | Simple, bien documenté | Sensible à la luminosité ambiante | À tester sous l'éclairage réel |
| Tri par poids (balance) | Produit du commerce | Fiable, peu de composants | Ne distingue pas verre et plastique de même poids | Écarté : ne répond pas au besoin |
| Vision par caméra | Forum robotique | Précis, flexible | Complexe à mettre en œuvre dans le délai | Écarté pour ce projet, piste pour une v2 |

## Pré-étude de faisabilité

{: .a_modifier }
> Quels points techniques vous inquiétaient, et comment les avez-vous testés
> rapidement (montage sur platine d'essai, pièce imprimée de test…) ? Résultats ?
> Vous pouvez résumer ici et détailler les protocoles et mesures dans la page
> [Tests et résultats](tests.md), avec un lien vers la section concernée.

Exemple : test du capteur de couleur sous l'éclairage réel sur 30 déchets :
27 correctement identifiés.

## Cahier des Charges
Projet : Machine That Draws

1. Présentation
La Machine That Draws est une machine automatisée capable de réaliser des dessins sur une feuille de papier à l'aide d'un stylo commandé par ordinateur. Son objectif est de reproduire des tracés de manière automatique et précise.


2. Besoin
Permettre à un utilisateur de réaliser automatiquement un dessin à partir d'instructions numériques.


3. Fonctions principales
-Dessiner
Réaliser des tracés sur une feuille.
Reproduire un dessin de manière fidèle.

-Déplacer le stylo
Déplacement sur les axes X et Y.
Respect des coordonnées du dessin.

-Lever et abaisser le stylo
Commencer ou arrêter le tracé.
Éviter les marques parasites.

-Exécuter un programme
Recevoir des commandes depuis un ordinateur.
Réaliser automatiquement les mouvements demandés.


4. Contraintes techniques
Carte Arduino.
Moteurs pas à pas.
Servomoteur pour le porte-stylo.
Structure mécanique conçue par l'équipe.
Modélisation réalisée sous OnShape.


5. Critères de performance
Critère	Exigence
Précision	Dessin fidèle au modèle
Répétabilité	Même résultat à chaque exécution
Fiabilité	Fonctionnement stable
Sécurité	Aucun danger pour l'utilisateur
Qualité du tracé	Traits propres et lisibles


6. Livrables
Fin du Semestre 1
Prototype fonctionnel (POC)
Présentation technique
Modèle CAO OnShape
Vidéo de démonstration
Fin du Semestre 2
Machine finale opérationnelle
Rapport technique
CAO complète
Soutenance du projet
Présentation publique de la machine


7. Validation
La machine sera considérée comme valide si :
Elle dessine automatiquement.
Elle suit correctement un trajet programmé.
Le stylo se lève et s'abaisse correctement.
Les dessins sont reproductibles.
Le système fonctionne de façon fiable. 


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
