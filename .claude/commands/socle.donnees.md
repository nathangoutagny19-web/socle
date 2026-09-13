---
description: Porte 4 — la base. Le schéma et les règles d'accès, dérivés du cadre et de la méthode. Produit socle/04-donnees.md et la migration.
---

Lis `socle/01-cadre.md`, `socle/02-methode.md`, `socle/03-arbitrages.md`.
S'il en manque un, arrête.

C'est la première commande qui nomme une technologie. Elle la nomme **parce que
le régime de souveraineté a été tranché à la porte 1**, pas l'inverse.

## La technologie suit le régime

| Régime tranché en porte 1 | Ce que tu proposes |
|---|---|
| 1 — les données peuvent sortir | PostgreSQL géré, hébergement au choix |
| 2 — Europe | PostgreSQL géré sur région européenne, contrat de sous-traitance à lire |
| 3 — rien ne sort | PostgreSQL sur l'infrastructure du cabinet |

Dans les trois cas : **PostgreSQL**, et le schéma est le même. C'est le point à
faire comprendre au cabinet — le régime change l'hébergeur, pas son système.
Il pourra changer d'avis sans tout refaire.

## Refus

- Tu ne proposes pas une technologie qui contredit le régime. Jamais, même si
  elle est plus simple.
- Tu n'écris pas une table qui n'existe pas dans `02-methode.md`.
- Tu ne mets **aucun seuil, aucune pondération, aucun barème en dur**. Ils vivent
  dans une table, modifiable sans développeur. C'est la méthode du cabinet, elle
  doit rester la sienne.

## Interroge avant d'écrire

- que doit-il se passer quand on supprime un client dont les missions sont
  archivées : refus, cascade, ou anonymisation ?
- qu'est-ce qui doit rester consultable après la fin d'une mission, et combien
  de temps
- faut-il pouvoir retrouver qui a modifié quoi, et quand — et cette trace est-elle
  une obligation contractuelle, réglementaire, ou un confort
- un rapport validé doit-il rester lisible tel quel dans cinq ans, même si les
  critères ont changé depuis

Cette dernière question décide si tu figes une copie du rapport ou si tu le
recalcules à la lecture. Les deux sont défendables, le cabinet doit choisir.

## Produis

`socle/04-donnees.md` — le schéma en français : chaque table, à quoi elle sert,
d'où viennent ses colonnes dans `02-methode.md`.

Une migration SQL, un seul fichier :

- clés primaires `uuid`, `created_at`, `updated_at` partout
- clés étrangères explicites, avec le comportement de suppression décidé ci-dessus
- une table `criteres` portant seuils et pondérations
- une table `journal` : qui, quoi, quand, valeur avant, valeur après
- **une politique RLS par rôle**, reprise du tableau de la porte 1, chacune
  commentée en français au-dessus de sa définition
- des **tests SQL qui vérifient qu'un rôle ne peut PAS lire ce qui ne le regarde
  pas** — un test par ligne du tableau des rôles, et ils doivent échouer si on
  retire la politique

Ce dernier point n'est pas négociable. Une politique RLS sans test qui la vérifie
est une intention, pas une sécurité.

## Porte

Écris en fin de `04-donnees.md` la liste des rôles de la porte 1 avec, en face,
la politique qui les applique. **S'il manque une politique pour un rôle, dis-le
et ne passe pas à la suite.**

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
