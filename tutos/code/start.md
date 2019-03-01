# Comment participer à la documentation de la Fabrique du Loch?

## Etape 1

### Avoir les outils de travail pour participer
- Atom, Sublime Text ou tout autre éditeur de texte permettant de gérer une arborescence fichiers en même temps.

#### Un éditeur de texte performant
Nous recommandons Atom ou SublimeText utilisés aujourd'hui par la plupart des
développeurs travaillant sur les technologies actuelles.

Ces éditeurs permettent de formater et coloriser du code d'un grand nombre de langages.

Ils permettent de gérer l'arborescence des fichiers de code-source (et de documentation).

Autre avantage, une extension pour la gestion de Github est intégrée à ces éditeurs
ne nécessitant pas d'autres logiciels.


#### Avoir un compte Github


##### Inscrire son compte Github à la Fabrique du Loch


### Travailler sur un projet existant
Cette page n'est pas claire?

Profitons-en, modifions-là!


## Etape 2

### Créer un nouveau projet

Pour créer un nouveau projet, nous allons simplifier l'initialisation en copiant
un projet existant, que nous allons utiliser comme modèle.

Cette opération sur Github est un *fork*.
[Le site modèle](http://fabloch.github.io/squid-modele)

Le projet est composé de plusieurs fichiers nécessaires pour la génération de pages web
avec Github Pages.

Inspecter le projet en utilisant la plateforme web de Github.




### Modifier le modèle

```
./_config.yml

```

Ce fichier contient une seule information, le thème utilisé par le générateur de pages.

```
theme: jekyll-theme-cayman

```

#### Le fichier default.html

```
./_layouts/default.html

```

Dans le répertoire **./layouts**, le fichier **default.html** contient le html
pour produire une page web à partir des fichiers .md.

[Fichier default.html](./_layouts/default.html)

Dans ce fichier, identifier la section **content**.
C'est elle qui injecte le contenu du fichier .md dans le code html.
C'est ainsi que la page est construite!

#### Les styles

Des feuilles de style sont appliquées au contenu.

Par défaut, des styles sont appliqués par le modèle dont on peut trouver ici une copie:

```
./assets/template.full.scss

```
**Ce fichier ne doit pas être modifié**; il ne contient qu'une copie des styles appliqués par défaut par le modèle déclaré dans le fichier **./_config.yml**

Pour modifier un style, il faut identifier **la classe css** que l'on souhaite modifier en inspectant le rendu de la page web en utilisant un navigateur web.

**Mozilla Firefox** permet de voir l'application des feuilles de style css et la structuration du html.
Il permet aussi de débugguer le code javascript s'exécutant dans un navigateur javascript.
(Il est intéressant de savoir manipuler ces outils conçus pour les développeurs qui permettent notamment
de comprendre les échanges entre une page web et des serveurs distants.)

Une fois le style à modifier identifié, on le cherche dans le fichier ./assets/template.full.scss.
On le copie das le fichier style.css.
On le modifie à volonté!

```
./assets/style.scss

```
