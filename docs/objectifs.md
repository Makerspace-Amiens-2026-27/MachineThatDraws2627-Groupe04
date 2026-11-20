---
layout: default
nav_order: 2
title: Objectifs du projet
---

# Objectifs du projet

{: .a_supprimer }
> Cette page pose le besoin **avant** toute solution technique : on y dit *quoi*
> faire, pas *comment*. Répondez aux questions de chaque section, puis supprimez-les.
> Voir [Définir son besoin et son cahier des charges](https://doc.makerspace-amiens.fr/workshops/methodologie-de-projet/concepts/definir-son-besoin/).

## Contexte

{: .a_modifier }
> D'où vient le projet ? Qui l'a demandé ? Dans quel cadre (cours, concours, commande) ?


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

{: .a_modifier }
> Listez les fonctions attendues avec des critères **mesurables** :
> **FP** pour une fonction principale (ce que le projet doit faire),
> **FC** pour une fonction contrainte (ce à quoi il doit s'adapter).
> Flexibilité : de F0 (impératif) à F3 (négociable). Exemple :

| Fonction | Critère | Niveau attendu | Flexibilité |
|---|---|---|---|
| FP1 : trier les déchets | Taux de tri correct | ≥ 80 % sur 20 essais | F1 |
| FP2 : informer le visiteur | Lisibilité du panneau | Lisible à 2 m | F2 |
| FC1 : s'alimenter | Autonomie sur batterie | ≥ 4 h | F0 |
| FC2 : s'intégrer au tapis | Largeur | ≤ 1 m | F0 |
