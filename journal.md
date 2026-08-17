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

## 2026-08-11 · Phase 1 · Session 2 · 2h00

**Fait** — Configuration de systemd : écrit une unit pour le worker Horizon,
testé `Restart=always` en tuant le processus à la main.

**Compris** — La différence entre `systemctl enable` (au démarrage) et
`systemctl start` (maintenant). Je confondais les deux depuis le début.

**Bloqué** — `journalctl` me renvoie les logs de toutes les instances de la unit
depuis le premier boot ; je n'ai pas trouvé comment ne voir que le dernier
démarrage. À creuser.

**Demain** — Reprendre par `journalctl` (options de filtrage), puis attaquer les
timers systemd.

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
