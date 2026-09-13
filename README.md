# Socle

Neuf commandes pour construire le système qui produit vos rapports clients.
Pour les cabinets de conseil et les bureaux d'études.

Ce n'est pas une bibliothèque de prompts. C'est une suite de portes : chacune
produit un document, et la suivante refuse de démarrer tant que ce document
n'est pas validé.

## À qui ça sert

**Si vous construisez vous-même**, vous collez les commandes dans Claude Code et
vous répondez aux questions. Le kit ne vous demandera jamais d'écrire du code.

**Si vous le faites construire**, vous le lisez et vous vérifiez qu'on vous pose
bien ces questions-là. Un prestataire qui ne vous demande pas où vivent vos
données, ni ce qu'un consultant qui part emporte avec lui, construira son outil,
pas le vôtre.

Le test est le même dans les deux cas.

## Les neuf portes

| | Commande | Ce qu'elle produit | Ce qu'elle refuse |
|---|---|---|---|
| 1 | `/socle.cadre` | Le régime des données, les rôles, ce qui se fige | De nommer une seule technologie |
| 2 | `/socle.methode` | Votre méthode sortie de vos fichiers | D'inventer une règle métier |
| 3 | `/socle.questions` | Chaque ambiguïté tranchée, et par qui | De trancher à votre place |
| 4 | `/socle.donnees` | Le schéma, les accès, les tests | De mettre un seuil en dur |
| 5 | `/socle.roles` | L'authentification, et ce qui n'est **pas** protégé | De cacher un bouton et d'appeler ça sécuriser |
| 6 | `/socle.plan` | La navigation, sur une page | D'écrire une ligne de code |
| 7 | `/socle.verif` | Les contradictions entre les six pages | De minimiser un écart |
| 8 | `/socle.construire` | Un lot à la fois | De démarrer s'il reste un écart grave |
| 9 | `/socle.boucle` | Vos corrections réinjectées | De transformer une correction en règle toute seule |

## Installer

Copiez le dossier `.claude/commands/` à la racine de votre projet, puis ouvrez
Claude Code. Les commandes apparaissent quand vous tapez `/socle`.

```bash
git clone https://github.com/nathangoutagny19-web/socle
cp -r socle/.claude/commands votre-projet/.claude/
```

Commencez par `/socle.cadre`. N'en sautez aucune.

## Ce qui le distingue

Les kits de développement assisté traitent l'hébergement et les droits d'accès
comme des détails d'implémentation, réglés à la fin.

Ici ce sont les portes 1 et 5, et rien ne passe sans elles. Parce que pour un
cabinet, la question n'est pas de savoir si le code compile. C'est de savoir où
partent les chiffres d'un client, qui peut les lire, et ce qui reste quand
quelqu'un s'en va.

Trois autres différences :

- **La porte 5 vous remet la liste de ce qui n'est pas sécurisé.** Un cabinet
  à qui on dit « c'est sécurisé » ne peut rien décider.
- **La porte 2 relève vos points de jugement**, les moments où vous tranchez ce
  qu'aucun calcul ne tranche. La porte 7 vérifie qu'aucun n'a été automatisé en
  route.
- **La porte 9 existe.** Vos corrections remontent dans le système. Sans elle,
  on vous automatise une photo de votre méthode.

## Ce qu'il ne fait pas

Il ne décide pas à votre place. Les réponses sont dans votre cabinet, pas dans
vos fichiers, et personne ne peut les donner pour vous.

Il ne remplace pas la relecture. Le texte que le système produit est un brouillon
tant qu'un humain ne l'a pas validé, et le kit vous empêche d'oublier cette règle.

## Licence

MIT. Le code que vous produisez avec est le vôtre, sur votre dépôt, sans condition.

Écrit par [Nathan Goutagny](https://www.natesystem.com), NateSystem.
