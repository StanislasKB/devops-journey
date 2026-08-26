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

## 2026-08-26 · Phase 1 · Session 9 · Durée 1h20

**Fait** - Cron,Crontab et Timer

**Compris** - Cron c'est le service qui permet d'exécuter les tâches planifiées et crontab c'est le fichier de configuration et en même temps une commande.
crontab -l pour lister les différentes conf de cron, crontab -e pour éditer et crontab -r pour tout effacer. Timer c'est le minuteur pour les services. On a les timers
en temps réels qui utilisent la directive OnCalendar et les timers monotones qui utilisent les directives comme OnActiveSec, OnBootSec. Un timer c'est comme une Unit Service,
d'ailleurs il agit sur les unit services.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec le lab libre.

---

## 2026-08-25 · Phase 1 · Session 8 · Durée 1h20

**Fait** - Linux Journey module « User Management » Lab sur Labex

**Compris** - /etc/sudoers contient la liste des utilisations qui ont les permissions sudo ainsi que lesdites permissions. /etc/passwd contient la liste des utilisateurs. 
/etc/shadow contient la liste des mots de passe encryptés des utilisateurs. visudo permet d'éditer /etc/sudoers de sorte qu'il puisse checker les erreurs de syntaxe pour
prévenir les erreurs de conf. On peut modifier /etc/passwd avec vipw mais le mieux c'est d'utiliser les commandes useradd, usermod, userdel.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec cron et timers systemd.

---

## 2026-08-24 · Phase 1 · Session 7 · Durée 1h15

**Fait** - Linux Journey module « The FileSystem »

**Compris** - /etc/fstab contient la conf du système de fichier. Inode c'est la table qui contient les metadata d'un fichier. MBR et GPT sont des tables de partition.
df permet de voir l'usage d'un disque et du l'utilisation d'espace d'un fichier. lsof permet de voir les fichiers ouverts. parted est la commande qui permet de partitionner un disk aussi bien MBR que GPT. Sa version graphique c'est gparted. On utilise mount et umount pour monter un disk. C'est une commande qu'on peut utiliser sur toutes les distributions 
Linux. Pour reparer le système de fichier on utilise fsck. On a aussi des commandes pour le swap. swapon open pour activer swapoff pour désactiver et mkwsap pour initialiser.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec utilisateurs, groupes, sudo.

---
     
## 2026-08-21 · Phase 1 · Session 6 · Durée 1h

**Fait** - Architecture de server bootstrap

**Compris** - Il y a aura plusieurs modules. trap et set euo pipeline

**Bloqué** - Quoi mettre dans le module 00 et 10.

**Demain** - Continuer avec le bilan hebdomadaire.

---

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
