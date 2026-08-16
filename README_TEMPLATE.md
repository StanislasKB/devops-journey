<!--
====================================================================
MODÈLE DE README — un par dépôt de phase.

À remplir PENDANT le projet, pas à la fin : les arbitrages s'oublient
en quelques jours.

Chaque section répond à une question que se pose le lecteur (client,
recruteur, lead technique) qui accorde ~90 secondes à ton dépôt :

  Titre + accroche  → « C'est quoi, en une phrase ? »
  Le problème       → « Ça sert à quoi ? Quel problème réel ? »
  Le résultat       → « Qu'est-ce que ça produit concrètement ? »
  Structure         → « Comment c'est fait ? »
  Décisions         → « Est-ce que ce type réfléchit, ou a-t-il suivi un tuto ? »

La section « Décisions et arbitrages » est celle qui fait la différence.
Si tu ne dois en soigner qu'une, c'est celle-là.

--------------------------------------------------------------------
CE QUE « STRUCTURE / ARCHITECTURE » VEUT DIRE SELON LA PHASE :

  Phase 1 — script bootstrap : liste ordonnée des étapes + état final
            du serveur (composants et versions). Pas de diagramme.
  Phase 2 — stack Docker : schéma des conteneurs et de leurs liens +
            tableau des étapes du build multi-étapes.
  Phase 3 — architecture AWS : vrai diagramme avec icônes AWS
            (VPC, zones, sous-réseaux, flux).
  Phase 4 — Terraform : arbre des modules et dépendances + diagramme
            de l'infrastructure produite.
  Phase 5 — CI/CD : diagramme du pipeline (déclencheurs, étapes,
            portes d'approbation, chemin de rollback).
  Phase 6 — EKS : schéma du cluster (namespaces, deployments, ingress,
            chemin IRSA).
  Phase 7 — observabilité : flux de télémétrie
            (source → collecte → stockage → visualisation → alerte).

Outils : Mermaid (rendu nativement par GitHub, le plus maintenable),
Excalidraw, diagrams.net + AWS Architecture Icons.
====================================================================
-->

# <nom-du-projet>

> Une phrase. Ce que ça fait, pour qui, et le bénéfice.
> Pas de contexte, pas de « projet réalisé dans le cadre de ma formation ».

## Le problème

Deux à quatre phrases sur la douleur réelle. Chiffrée si possible : combien de
temps perdu, combien d'erreurs, combien ça coûte.

## Le résultat

Ce qu'on obtient concrètement. La commande à lancer, et ce qui se passe.
Idéalement avec un chiffre : durée, taille, coût mensuel.

```bash
# la commande
```

## Structure / Architecture

<!-- diagramme, arbre de fichiers ou liste ordonnée des étapes —
     voir l'en-tête de ce fichier pour la forme adaptée à ta phase -->

## Décisions et arbitrages

| Décision | Alternative écartée | Pourquoi |
|---|---|---|
|  |  |  |
|  |  |  |
|  |  |  |

Trois à cinq lignes. Chaque ligne doit contenir une alternative réelle, pas un
homme de paille.

> **Si rien ne te vient :** relis ton `journal.md` de la phase. Chaque ligne
> « Bloqué » est une décision déguisée — tu as buté, cherché, choisi.

## Utilisation

```bash
# prérequis
# puis la ou les commandes
```

## Limites connues

- Ce que ça ne fait pas, et qui pourrait surprendre
- Ce que tu ferais différemment avec plus de temps ou de budget
- Ce qui est volontairement hors périmètre, et pourquoi

## Ce que j'en ai retiré

Trois lignes maximum. Techniques, pas émotionnelles.
