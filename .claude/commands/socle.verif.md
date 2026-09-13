---
description: Porte 7 — la vérification croisée. Chercher les contradictions entre les six pages avant de construire. Produit socle/07-verif.md.
---

Lis les six pages du dossier `socle/`.

Cette commande ne construit rien et n'améliore rien. Elle cherche les
contradictions. C'est la seule porte dont le travail est de **trouver des
problèmes**, et elle échoue si elle n'en trouve aucun.

## Refus

- Tu ne corriges rien ici. Tu constates et tu nommes.
- Tu ne minimises aucun écart. Pas de « point mineur », pas de « à voir plus tard ».
- Tu ne valides pas pour faire plaisir.

## Les croisements à faire

**Cadre contre données.** Chaque contrainte de la porte 1 est-elle appliquée
quelque part dans le schéma ? Nomme le fichier et la ligne. Sinon : écart.

**Rôles contre politiques.** Chaque ligne du tableau des rôles a-t-elle sa
politique RLS et son test ? Un rôle sans test est un écart, pas un détail.

**Méthode contre schéma.** Chaque objet de `02-methode.md` existe-t-il en base ?
Chaque table a-t-elle une origine dans la méthode ? Une table sans origine est
une invention : nomme-la.

**Jugement contre plan.** Chaque point de jugement relevé en porte 2 est-il
laissé à un humain dans le plan ? Si l'un d'eux est devenu un calcul automatique,
c'est l'écart le plus grave du kit. Signale-le en premier.

**Arbitrages contre tout le reste.** Chaque décision de `03-arbitrages.md` est-elle
respectée ? Une décision contredite sans que personne ne l'ait rouverte est un écart.

**Souveraineté contre technologies.** Chaque service nommé dans les pages 4 à 6
est-il compatible avec le régime de la porte 1 ? Un seul service hors régime
suffit à rendre l'ensemble non conforme.

**Attentes.** Reste-t-il des `[EN ATTENTE]` ? Lesquels, et qu'est-ce qui est
construit dessus.

## Produis

`socle/07-verif.md` :

- les écarts, classés du plus grave au plus léger, chacun avec les deux endroits
  qui se contredisent
- pour chacun : ce qu'il faut rouvrir, et à quelle porte
- la liste de ce qui est vérifié et sain, pour que le cabinet sache ce qui a été
  regardé

## Porte

**Tant qu'il reste un écart grave, `/socle.construire` ne démarre pas.**
Dis-le clairement et renvoie vers la porte concernée.

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

**Les réserves ouvertes.** Si une porte précédente a été franchie sous réserve,
rappelle en tête ce qui est construit sur du sable, et qui le porte. Une réserve
qu'on oublie devient un défaut qu'on découvre devant le client.

**Tu ne clos pas la conversation.** Pas de « à demain », pas de « bonne soirée ».
Tu rends ton document, tu dis où en est la porte, tu t'arrêtes là.
