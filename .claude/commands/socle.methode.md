---
description: Porte 2 — la méthode. Faire lire les fichiers existants et en extraire le modèle, sans technologie. Produit socle/02-methode.md.
---

Lis `socle/01-cadre.md` avant toute chose. S'il n'existe pas, arrête et renvoie
vers `/socle.cadre`.

Le cabinet produit déjà ses rapports. Sa méthode existe, elle est écrite en
morceaux : dans des tableurs, dans un document de consignes, dans des rapports
livrés, et dans la tête de deux ou trois personnes. Ton travail est de la sortir
de là, pas d'en inventer une meilleure.

## Refus

- Tu ne proposes **aucune** technologie. Ni base, ni langage, ni hébergeur.
- Tu n'écris **aucun** schéma SQL.
- Tu ne proposes rien avant d'avoir posé tes questions et reçu les réponses.
- Tu n'inventes **aucune** règle métier. Si le fichier ne la montre pas et que
  personne ne te la donne, elle est marquée `[À TRANCHER]`.

## Demande les pièces

Réclame, et attends de les avoir :

- deux ou trois tableurs de production, dont un vrai, mal rangé, avec ses
  onglets morts — pas une version nettoyée pour l'occasion
- le document de consignes de rédaction, dans sa dernière version
- deux rapports livrés à des clients différents, pour voir ce qui change
- s'il existe, le modèle de rapport vierge

## Lis, puis interroge

Après lecture, pose au minimum :

- quelles colonnes sont saisies à la main, lesquelles sont calculées ailleurs
- d'où vient chaque donnée importée, et qui la produit
- ce qui change d'un client à l'autre, et ce qui ne change jamais
- ce qui est saisi deux fois dans la chaîne, et laquelle des deux copies fait foi
- les seuils et les pondérations : où sont-ils écrits, qui a le droit de les changer
- les cas particuliers que les fichiers ne montrent pas — le client hors norme,
  l'année incomplète, la donnée manquante
- à quel moment quelqu'un décide quelque chose qu'aucun calcul ne peut décider

Cette dernière question est la plus importante. Note la réponse mot pour mot :
c'est le jugement du cabinet, et il ne doit jamais être automatisé.

## Produis

Écris `socle/02-methode.md` :

- **les objets** : ce que le cabinet manipule, en français métier — mission,
  client, critère, relevé, rapport. Un paragraphe chacun.
- **ce qui les relie**, en phrases : « une mission porte sur un client et produit
  un rapport », pas en diagramme.
- **les règles de calcul**, chacune avec sa source : quel fichier, quelle cellule,
  qui l'a écrite.
- **les points de jugement** : les moments où un humain tranche. Repris mot pour mot.
- **`[À TRANCHER]`** partout où tu as dû deviner.

Aucun nom de table. Aucun type SQL. Cette page doit être relisible par l'associé
qui signe les rapports.

## Porte

Compte les `[À TRANCHER]`. S'il y en a, enchaîne sur `/socle.questions`.
S'il n'y en a aucun, tu as probablement inventé. Relis et sois plus honnête.

## Convergence — la règle qui vaut pour les neuf portes

**Tu poses les questions de cette porte une fois.** Les questions que mes
réponses ouvrent, tu les écris dans « Non tranché » au lieu de me les poser.
Tu ne relances un tour que si une réponse rend le document impossible à écrire.

Une porte est un cadrage, pas une enquête sans fin. Ton livrable est le
document de la porte, avec ce qui manque nommé dedans — pas la résolution de
tout ce que tu as découvert en chemin.

**Tu ne gères pas mon agenda.** Pas de « demain matin », pas de rendez-vous,
pas de suivi sur plusieurs jours. Tu cadres un système ; ce que j'en fais dans
ma semaine ne te regarde pas.
