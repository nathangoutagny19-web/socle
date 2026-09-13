---
description: Porte 8 — la construction. Un lot à la fois, validé avant le suivant. Met à jour socle/08-avancement.md.
---

Lis `socle/06-plan.md` et `socle/07-verif.md`.

**Si `07-verif.md` n'existe pas, ou s'il reste un écart grave : arrête.**
Dis lequel, et renvoie vers la porte concernée.

## Refus

- Tu ne construis **qu'un lot à la fois**, celui que le cabinet désigne.
- Tu ne prends aucune décision laissée `[EN ATTENTE]`. Tu t'arrêtes et tu demandes.
- Tu n'ajoutes aucune fonctionnalité qui n'est pas dans le plan, même utile,
  même rapide. Tu la notes dans « À rouvrir » et tu continues.
- Tu ne remplaces jamais un point de jugement par un calcul.

## Procède, lot par lot

Pour chaque lot :

1. Rappelle ce que le lot contient, en trois lignes.
2. Écris le code. Le schéma d'abord, les écrans ensuite.
3. Écris les tests qui vérifient les règles d'accès du lot — pas les tests
   d'affichage, les tests de sécurité.
4. Montre ce qui est utilisable **tout de suite**, et comment le vérifier soi-même.
5. Liste ce que tu as dû supposer.
6. **Arrête-toi et attends la validation.**

## À la fin de chaque lot

Mets à jour `socle/08-avancement.md` :

- les lots livrés, avec leur date
- ce qui a été supposé, lot par lot
- « À rouvrir » : ce qui a été écarté en route et mérite une décision

## Porte

Quand tous les lots du plan sont livrés, ne déclare pas le chantier terminé.
Enchaîne sur `/socle.boucle` : un système qui ne se corrige pas se périme.

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
