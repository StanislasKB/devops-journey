# Journal — Roadmap DevOps & AWS

Objectif : expert DevOps / Cloud AWS : août 2026 → août 2027.
Une entrée par session, rédigée **à la fin de la session**, jamais le lendemain.
Les entrées les plus récentes en haut.

Créneau : lundi–vendredi 06h35–08h35 · samedi 06h30–10h30.
Les bilans hebdomadaires et trimestriels vont dans `bilans.md`, pas ici.

---

## 2026-09-16 · Phase 1 · Session 23 · Durée 35min

**Fait** - HTTP
**Compris** - Les en-têtes HTTP sont des informations supplémentaires que le client ou le serveur s'envoient. Méthode HTTP : TRACE
Keep-alive permet de réutiliser une connection TCP au lieu d'en créer de nouvelle à chaque fois et HSTS indique au navigateur d'utiliser
HTTPS à chaque fois pendant une période donnée. HEAD permet d'obtenir les métadonnées d'une ressource.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec server-bootstrap.

---

## 2026-09-16 · Phase 1 · Session 21 · Durée 1h

**Fait** - TLS et Certificats
**Compris** - Le handshake : le navigateur envoi un premier en guise de Hello les versions de TLS et la suite crypotographique qu'il peut
utiliser. Il envoi aussi une key_share. Le serveur répond avec une version de TLS (la plus récente c'est la 1.3) et une key_share mais aussi
un certificat et sa clé publique. Le navigateur vérifie si le certificat est sûr. Si cette phase de négociation se passe bien une connection
est établie et désormais toute la communication se fait de manière sûre avec les chiffrement. 

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec Lab libre.

---

## 2026-09-15 · Phase 1 · Session 20 · Durée 50min

**Fait** - Dns:messagerie

**Compris** - MX indique quel serveur reçoit les messages pour le domaine. SPF(Sender Policy Framework) indique qui peut envoyer les messages au nom du domaine. Dans une
configuration on a un seul enregistrement SPF. DKIM(DomainKeys Identified Mail) s'occupe de signer les messages. On laisse une clé privée sur le serveur et la clé publique
dans l'enregistrement DNS. Le message sera signé grâce à ses éléments permettant ainsi de s'assurer qu'il n'a pas été modifié. DMARC(Domain-based Message Authentication, Reports
and Conformance) s'occupe de l'alignement et de la politique. C'est à ce niveau qu'on décide ce qui sera fait si un mail n'est pas aligné. Un message est aligné si au moins l'un 
SPF ou DKIM passe. Au niveau du DMARC on peut rejeter, mettre en quarantaine ou observer. 

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec TLS et certificats.

---

## 2026-09-14 · Phase 1 · Session 19 · Durée 1h

**Fait** - Dns:résolution

**Compris** - Lorsqu'un client tape un nom de domaine dans son navigateur, il le résolveur stub qui regarde dans son cache pour voir s'il a l'adresse IP;
s'il n'a pas l'adresse IP il regarde s'il a l'adresse du serveur d'autorité de domaine, sinon il vérifie pour les serveurs TLD et root. S'il n'a aucune de ces 
informations, il va envoyer la demande au résolveur dns, qui lui va aussi vérifier dans son cache. Dans le cas où il y a un élément dans le cache certaines étapes 
sont sautées. Sinon, le résolveur contact les serveurs root (ils sont au nombre de 13), il aura en retour une réponse avec l'IP du serveur TLD. Il va ensuite contacter
le serveur TLD qui va lui répondre avec l'adresse IP du serveur d'autorité de domaine ou encore serveur de domaine de référence. En contactant ce dernier, il aura l'adresse
IP dont le serveur a besoin pour contacter et utiliser le service. nslookup et dig sont des commandes qu'on peut utilise pour diagnostiquer un DNS. On a plusieurs types
d'enregistrements DNS, mais les plus courants sont : A pour les IPv4, AAAA pour les IPv6, CNAME (Canonical Name) pour les alias(autres noms de domaines), TXT pour les notes,
MX(Exchange Mail) pour les mails liés au domaine. On a aussi: CAA, PRT, SRV, etc.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec DNS:messagerie.

---

## 2026-09-12 · Phase 1 · Session 18 · Durée 45min

**Fait** - Module 40-php

**Compris** - On peut créer des pool spécifiques pour les sites et des socket spécifiques (Ex: php8.4-laravel.sock au lieu de php8.4-fpm.sock) que nginx peut utiliser.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec le BILAN HEBDOMADAIRE.

---

## 2026-09-10 · Phase 1 · Session 16 · Durée 50min

**Fait** - Lab libre

**Compris** - Rien de nouveau j'ai repratiqué et mieux gardé le découpage vlsm

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec le débogage.

---

## 2026-09-08 · Phase 1 · Session 14 · Durée 1h40

**Fait** - Découpage en sous réseaux

**Compris** - Découpage classique et méthode VLSM pour le découpage dynamique. ça a été un rappel des choses que je maitrisais avant. 

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec la table de routage.

---

## 2026-09-07 · Phase 1 · Session 13 · Durée 1h20

**Fait** - Practical Networking, série « Packet Traveling » 4 exercices subnettingpractice.com

**Compris** - L1 transporte les bits, L2 assure la livraison saut à saut, L3 assure la livraison bout en bout, L4 assure la livraison service à service.
Le protocole ARP est utilisé au niveau des routeurs afin de connaître l'adresse MAC inconnue d'un device dont l'adresse IP est connue.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec découpage, calcul de plages.

---
## 2026-08-29 · Phase 1 · Session 12 · Durée 1h

**Fait** - modules 20 et 30

**Compris** - source permet de charger les variables qui sont dans un fichier dans le script afin de pouvoir les utiliser.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec bilan hebdomadaire.

---

## 2026-08-28 · Phase 1 · Session 11 · Durée 1h20

**Fait** - Débogage, 2 Sad Servers

**Compris** - lsof ouvre les fichiers en cours. Avec fuser -k on peut tuer un processus lié à un fichier. On a aussi iostat, vmstat pour le monitoring.
Pour un monitoring continue on peut utiliser sar du package sysstat.

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec server-bootstrap.

---
## 2026-08-27 · Phase 1 · Session 10 · Durée 1h20

**Fait** - Lab Libre 3 sad Server niveau easy

**Compris** - cut, sort, uniq, grep, fuser, ps

**Bloqué** - Rien de bloquant aujourd'hui.

**Demain** - Continuer avec le débogage.

---

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
