---
description: Porte 1 — le cadre. Ce qui ne se négocie pas avant d'écrire une ligne. Produit socle/01-cadre.md.
---

Tu ouvres un chantier : un cabinet de conseil ou un bureau d'études veut produire
ses rapports clients depuis un seul système, au lieu d'une chaîne de fichiers.

Ton rôle ici n'est pas de proposer. C'est d'établir ce qui ne se négocie pas.

## Refus

- Tu ne proposes **aucune** technologie dans cette commande. Pas de nom d'hébergeur,
  pas de nom de base, pas de nom de modèle.
- Tu n'écris **aucun** code.
- Tu ne passes pas à la suite tant que le régime de souveraineté n'est pas tranché.

## Interroge, et attends les réponses

Pose ces questions une par une. Si une réponse est vague, redemande.

**Le régime des données.** Un seul des trois :
1. elles peuvent sortir — aucune contrainte
2. elles restent en Europe — le cas le plus fréquent
3. elles ne sortent pas de chez vous — défense, nucléaire, secret industriel

Demande sur quoi repose la réponse : un contrat client, une clause de marché,
une politique interne, ou une préférence. **Ce n'est pas la même chose, et la
suite en dépend.**

**Si la réponse est « un contrat » ou « une clause de marché », réclame l'extrait.**
Pas un résumé de mémoire : le passage. Tant qu'il n'est pas lu, le régime est
*déclaré*, pas établi — et un régime déclaré qui s'effondre à la lecture emporte
les huit portes suivantes. C'est un blocage à part, pas une ligne de « Non tranché ».

Vérifie aussi que la réponse est bien un seul régime. Si une contrainte plus dure
s'applique à une partie des données — « ça, ça ne sort jamais, même en Europe » —
le cadre est **mixte**, et tu le dis. Une zone plus stricte à l'intérieur d'un
régime large impose soit de la séparer pour de bon, soit de durcir tout le reste.
Le cabinet doit choisir lequel des deux, et le savoir maintenant.

**Ce qui sort du cabinet.** Y a-t-il des données qui ne doivent jamais être
envoyées à un service tiers, même européen ? Lesquelles, et pourquoi.

**Les personnes.** Le rapport contient-il des données personnelles au sens du
RGPD — noms, fonctions, salaires, évaluations, santé, absences ? Combien de temps
doivent-elles être conservées, et qui a décidé de cette durée.

**La propriété.** À qui appartient le code produit ? Si c'est un prestataire qui
construit, sur quel compte vit le dépôt. Réponse attendue : le compte du cabinet.

**Les rôles.** Liste les personnes qui ouvriront l'outil, par fonction, pas par
prénom. Pour chacune : ce qu'elle doit voir, ce qu'elle doit pouvoir modifier, et
ce qu'elle ne doit jamais voir.

**Qui affecte les missions.** Si un rôle est limité à « ses missions », demande qui
décide qu'une mission est la sienne, et à quel moment. Sans cette réponse, « ses
missions » ne veut rien dire, et la porte 5 se construira dans le vide.

**Le client final.** Accède-t-il à l'outil, ou seulement à un rapport figé qu'on
lui remet ? Les deux réponses sont valables, elles ne construisent pas la même chose.

**Ce qui se fige.** Qu'est-ce qui, une fois validé, ne doit plus jamais redevenir
modifiable ? Un rapport remis, un chiffrage signé, une note d'étape.

## Produis

Écris `socle/01-cadre.md` :

- le régime retenu, et sur quoi il repose
- la liste nominative des contraintes, chacune avec sa source
- le tableau des rôles : rôle, lit, écrit, ne voit jamais
- ce qui se fige, et à quel moment
- **une section « Non tranché »** listant chaque question restée sans réponse ferme

Termine par l'une de ces deux lignes, jamais une autre. **Une porte bloquée qui
se déclare franchie rend tout le dossier suspect :**

- `Porte 1 franchie le <date>. Régime : <1|2|3>.`
- `Porte 1 NON franchie le <date>. Régime : <1|2|3> déclaré, non établi. Reste : <n> points.`

## Porte

S'il reste une ligne dans « Non tranché », dis-le et **ne propose pas de passer
à `/socle.methode`**. Rends la main au cabinet avec la liste des questions ouvertes.

Et si le régime repose sur un contrat dont l'extrait n'a pas été lu, dis-le
séparément, en tête : ce n'est pas une question ouverte parmi d'autres, c'est le
sol sur lequel tout le reste est posé.
