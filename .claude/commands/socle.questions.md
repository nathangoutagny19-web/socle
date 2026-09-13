---
description: Porte 3 — les questions qui bloquent. Forcer la résolution de chaque [À TRANCHER] avant de concevoir. Met à jour socle/02-methode.md.
---

Lis `socle/01-cadre.md` et `socle/02-methode.md`.

Cette commande existe pour une seule raison : **une ambiguïté non tranchée
maintenant devient un défaut dans le logiciel, et on la découvre devant le client.**

## Refus

- Tu ne tranches **aucune** question à la place du cabinet.
- Tu ne proposes pas « une valeur par défaut raisonnable » pour avancer.
- Tu ne regroupes pas plusieurs questions en une pour aller plus vite.

## Procède

Reprends chaque `[À TRANCHER]`, un par un, dans l'ordre. Pour chacun :

1. Rappelle où tu l'as trouvé — quel fichier, quelle ligne.
2. Pose la question en une phrase, sans jargon.
3. Propose deux ou trois réponses possibles, avec **ce que chacune change
   concrètement dans le travail de tous les jours**, pas dans le code.
4. Attends la réponse. Ne passe pas à la suivante.

Si la réponse est « ça dépend », c'est que la question en cache deux. Découpe-la.

Si la réponse est « je ne sais pas, il faudrait demander à X », note-le tel quel
et marque la question `[EN ATTENTE — X]`. Ce n'est pas un échec, c'est un fait.

## Produis

Mets à jour `socle/02-methode.md` : chaque `[À TRANCHER]` devient soit une règle
écrite avec son auteur et sa date, soit un `[EN ATTENTE — X]`.

Écris `socle/03-arbitrages.md` : la liste des décisions prises, qui les a prises,
et ce qu'elles écartent. **Cette page est celle qu'on relit dans six mois quand
quelqu'un demande pourquoi l'outil fait ça.**

## Porte

Tant qu'il reste un `[EN ATTENTE]`, tu peux passer à `/socle.donnees` — mais tu
listes en tête du fichier ce qui est construit sur du sable, et tu le rappelles
à chaque commande suivante.
