---
layout: default
nav_order: 2
title: Objectifs du projet
---

# Objectifs du projet


## Contexte

Ce projet est réalisé dans le cadre du module « Machine That Draws » proposé par le MakerSpace d'Amiens. L'objectif est d'appliquer les connaissances acquises en conception mécanique, électronique, programmation et fabrication numérique à travers la réalisation d'une machine capable de dessiner automatiquement. Le projet est évalué à travers plusieurs livrables ainsi qu'une présentation lors de la Journée des Projets


## Problème et public cible

### Le problème

Dessiner à la main une image détaillée (hachures, aplats de couleurs, textes) demande beaucoup de temps et un geste très régulier. Les imprimantes classiques, elles, ne reproduisent pas l'aspect d'un vrai tracé au stylo. Les machines du commerce comme l'AxiDraw répondent à ce besoin, mais elles sont chères et fermées : on ne peut pas les modifier ni apprendre de leur conception.

Nous voulons une **machine à dessiner automatique, abordable et modifiable**, qui trace sur une feuille de papier une image vectorielle avec un vrai stylo, y compris avec plusieurs couleurs.

### Public cible

| Utilisateur | Besoin |
|---|---|
| Étudiants et makers du MakerSpace | Réaliser des dessins, affiches ou cartes personnalisées sans savoir bien dessiner |
| Enseignants et animateurs | Une démonstration concrète de mécanique, d'électronique et de programmation (G-code) |
| Curieux et amateurs d'art numérique | Transformer un fichier vectoriel en dessin « fait main » |

### Conditions d'utilisation

| Critère | Condition |
|---|---|
| Lieu | Intérieur, sur une table stable (atelier, salle de classe, MakerSpace) |
| Support | Feuille de papier au format A4 fixée sur le plateau, avec un stylo ou un feutre |
| Alimentation | Secteur, via un bloc d'alimentation |
| Utilisation | Sous surveillance d'un utilisateur, qui peut couper la machine à tout moment avec l'arrêt d'urgence |
| Compétences | Notions de base seulement : charger un fichier, lancer le tracé |
| Contraintes | Pièces mobiles : ne pas approcher les mains pendant le tracé. Machine non destinée à un usage par de jeunes enfants sans encadrement. |

## Cahier des charges

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
