---
description: Porte 5 — l'accès. Authentification, rôles, et la liste de ce qui n'est pas sécurisé. Produit socle/05-acces.md.
---

Lis `socle/01-cadre.md` et `socle/04-donnees.md`.

C'est ici que les projets se cassent. Une démo n'a pas de rôles ; un outil qu'on
ouvre à son équipe, puis à ses clients, n'existe pas sans eux.

## Refus

- Tu ne mets **jamais** le rôle dans le jeton côté client. Il vit en base.
- Tu ne protèges **jamais** une page uniquement à l'affichage. Cacher un bouton
  n'est pas une sécurité.
- Tu ne considères pas qu'une vérification côté serveur dispense de RLS. Les deux,
  toujours. Si on retire le front, la base doit tenir seule.
- Tu n'ajoutes pas de rôle qui n'était pas dans le tableau de la porte 1. S'il en
  manque un, retourne à la porte 1.

## Interroge

- qui crée les comptes, et **qui les supprime le jour où quelqu'un part** ?
- que se passe-t-il pour les dossiers d'un consultant qui quitte le cabinet ?
- un client accède-t-il à l'outil, ou seulement à un rapport figé ? (déjà tranché
  porte 1 — vérifie que la réponse tient toujours)
- que doit-il se passer si quelqu'un ouvre un dossier qui ne le regarde pas :
  page vide, message, ou alerte à quelqu'un ?
- combien de temps une session reste-t-elle ouverte sur un poste partagé ?
- y a-t-il une obligation de traçabilité, contractuelle ou réglementaire, et
  laquelle

## Produis

`socle/05-acces.md` :

- le mode d'authentification retenu, et pourquoi celui-là pour ce cabinet
- les rôles en base, dans une table `profils`, jamais ailleurs
- la protection des routes **côté serveur**, route par route
- le rattachement de chaque écran à un rôle, repris du tableau de la porte 1
- la durée de session, et ce qui la coupe
- le journal des accès aux dossiers clients : ce qui est enregistré, qui peut le lire

Puis, obligatoirement, une dernière section :

> ## Ce qui n'est pas sécurisé
>
> La liste de ce que cette porte ne couvre pas, en clair, sans atténuation.

Exemples de ce qui doit y figurer s'il n'a pas été traité : l'export de données
par un utilisateur légitime, les pièces jointes, les sauvegardes et qui peut les
restaurer, l'accès de l'hébergeur, les journaux applicatifs contenant des données
personnelles, la récupération de mot de passe, le poste de travail lui-même.

**Un cabinet qui sait ce qui n'est pas protégé peut décider. Un cabinet à qui on
dit « c'est sécurisé » ne peut rien décider du tout.**

## Porte

Si la section « Ce qui n'est pas sécurisé » est vide, tu n'as pas fait le travail.
Recommence.

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
