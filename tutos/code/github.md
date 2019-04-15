# Utiliser github

Git est un mécanisme de gestion des versions de fichiers.
Chaque nouvelle version d'un fichier est suivi pour permettre la synchronisation entre plusieurs machines.



## Fetch
La récupération des modifications venant du dépôt Github.

## Pull

Un pull est l'exécution de deux commandes

```
git fetch
git merge
```

## Commit
Mettre un message simple qui permet d'identifier ce qui a été fait sur les documents.
Ce message peut faire gagner beaucoup de temps lors de recherches ultérieures.
En général, on essaye de ne mettre dans un commit que des modifications complémentaires et ne traitant que d'un problème.

```
git add.
git status
git push -u origin master

```

Débrief, de mon côté, les points à traiter
```
- Outils: Slack pour comm, Github pour dépôt?
- Archi: Electron pour le moment, avant hébergement serveur
- Repo: localisation, ouverture, licences
```

## Push
```
git push

```
Pushing to origin

## Merge
L'intégration des modifications de deux historiques de modification.
C'est l'opération que l'on réalise lorsqu'on veut intégrer nos modifications dans le dépôt Github.
On doit tout d'abord vérifier qu'il n'y a pas de conflit.
Il se peut qu'une autre personne ait modifié des fichiers et les ait déjà remis dans le dépôt Github.
Un cas critique est la modification d'une même section dans un fichier.
La dernière personne opérant la fusion entre les deux versions doit sélectionner la version la plus à jour.

## Conflits
Dans Atom, l'éditeur vous demande de choisir entre les deux version du bloc de texte
pour lequel il y a un conflit.

## Branches
Dans un dépôt Github, on peut créer des branches.
Une branche permet de modifier un dépôt sans affecter la version.
