# Journal — Roadmap DevOps & AWS

Objectif : expert DevOps / Cloud AWS : août 2026 → août 2027.
Une entrée par session, rédigée **à la fin de la session**, jamais le lendemain.
Les entrées les plus récentes en haut.

Créneau : lundi–vendredi 06h35–08h35 · samedi 06h30–10h30.
Les bilans hebdomadaires et trimestriels vont dans `bilans.md`, pas ici.

---

<!-- ====================================================================
     MODÈLE À COPIER POUR CHAQUE SESSION
     (supprime ce bloc quand tu l'auras en tête)

## AAAA-MM-JJ · Phase X · Session N · Durée

**Fait** — Ce que tu as réellement fait. Concret, pas « j'ai révisé le réseau ».

**Compris** — La chose que tu ne savais pas ce matin. Si tu ne trouves rien,
écris-le : c'est une information en soi.

**Bloqué** — Ce qui reste flou ou cassé. C'est la ligne la plus importante :
elle devient le point de départ de la session suivante, et la matière première
de la section « Décisions et arbitrages » de tes README.

**Demain** — La première action de la prochaine session. Une phrase.

---
     ==================================================================== -->

## 2026-08-21 · Phase 1 · Session 5 · Durée 1h

**Fait** - Débogage. Casser la unit et vérifier avec journalctl. Bandit 15 à 17

**Compris** - L'option --since ou -S de journalctl permet de préciser une date, -u la unit, -f un mode de suivi.

**Bloqué** - Rien de bloquant aujourd'hui également.

**Demain** - Continuer avec le démarrage du server bootstrap.

---

## 2026-08-20 · Phase 1 · Session 4 · Durée 1h

**Fait** - Lab libre. Création d'une unit de worker laravel

**Compris** - On peut utiliser WorkingDirectory pour définir le dossier, User pour l'utilisateur en action, Group pour le group. RestartSec pour le délai avant restart.
 WantedBy reste dans Install.

**Bloqué** - Rien de bloquant aujourd'hui également.

**Demain** - Continuer avec le débogage.

---

## 2026-08-19 · Phase 1 · Session 3 · Durée 1h40

**Fait** - Systemd : création d'un service. Bandit niveau 13 à 15

**Compris** - On a différent type de service : simple, oneshot, forking, dbus... Start permet de lancer le service alors que enable active
le service pour un démarrage automatique au lancement du système. On peut créer un timer lié au service qui sera comme un cron pour le service.
ExecStart est la commande que le service va lancer au démarrage et ExecStop celle qu'il lancera à la fin. On aussi d'autres directives comme 
Restart, WantedBy. Lorsqu'un service est à restart always et on arrête le processus manuellement, un autre est crée.

**Bloqué** - Rien de bloquant aujourd'hui également.

**Demain** - Continuer avec le lab libre.

---

## 2026-08-18 · Phase 1 · Session 2 · 2h00

**Fait** - Linux Journey module  « Permissions » Bandit niveau 6 à 12.

**Compris** - Valeurs numériques des permissions (r=4,w=2,x=1). SETUID une permission qui permet de pouvoir exécuter
un program comme si on l'utilisateur en est le propriétaire. Symbole = s, valeur numérique 4. SETGID une permission 
qui permet d'exécuter un programme comme si on était membre d'un groupe ayant les permissions. Symbole =s, valeur 
numérique 2. STICKY BIT permission qui empêche un utilisateur autre que le owner de supprimer un fichier. 
Effective UID, Save UID, Real UID. find peut s'accompagner de -user -group aussi. chgrp tout comme chown mais pour changer le groupe. 

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Reprendre par systemd.

---

## 2026-08-17 · Phase 1 · Session 1 · 2h00

**Fait** - Linux Journey, modules « Command Line » et « Processes ».
OverTheWire Bandit, niveaux 0 à 6.

**Compris** - Le tild (~) c'est pour le home directory. find avec -size pour trouver un fichier donné en filtrant avec la taille. Pour ouvrir un fichier "-" il faut mettre le path. Les signaux qu'on envoi au process et leur rôle. Les différents états d'un process et ce qu'ils représentent chacun.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - permissions : chown, setuid.

---

<!-- Archivage : au-delà de trois ou quatre mois, déplace les entrées passées
     dans journal/AAAA-MM.md et ne garde ici que le mois en cours. -->
