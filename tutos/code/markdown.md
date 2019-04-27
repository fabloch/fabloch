# Les fichiers Markdown
En créant des fichiers .md, il est possible de créer des pages web alimentant un site partagé par les membres d'un groupe.

Les fichiers .md sont des fichiers texte que l'on peut écrire simplement.
Une fois publié, le fichier est présenté sous forme de page web.
Comme cette propre page!

## La syntaxe Markdown
En utilisant une syntaxe simple, il est possible de composer du texte structuré avec quelques conventions simples
pour créer des mises en gras, en italique, des titres, des listes, inclure des liens, des images, des tableaux, etc.


### Quelques exemples de mise en pages

# Titre 1
## Titre 2
### Titre 3

Texte en **Gras** ou _Italique_ ou `Code`

- Liste
- Non ordonnée

1. Liste
2. Numérotée

### Créer des liens vers d'autres pages, des Images

Pour créer un lien vers une autre page
```
[Lien](url)
```

Pour ajouter une image à la page courante
```
![Image](src)
```

Les images ont souvent besoin d'être redimensionnées.

Il est possible de le faire directement en contrôlant sa largeur:
```
![Image](src){: width="600px"}
```

#### Pour les pages et fichiers sur votre propre site
Inutile de spécifier des liens absolus (avec le scheme http), il suffit de spécifier le chemin vers l'url ciblée.

Depuis le répertoire racine du site:
```
/pictures/party.jpg = http://monsite.adresse/pictures/party.jpg
```

Il est préférable d'utiliser la syntaxe ./pictures/party.jpg qui indique que vous commencez le chemin depuis le répertoire de la page en cours.

```
./pictures/party.jpg
```

Depuis la page /2019/birthday.md, le code ci dessus adresse http://monsite.adresse/2019/pictures/party.jpg



### Un bloc de code (comme ci-dessus)
```

markdown
Voici un bloc de code.
(Certains éditeurs comme Atom, vous permettent de créer un bloc de code en tapant uniquement "code" sur une seule ligne.
Le bloc sera automatiquement créé, voir plus bas).

```

Ces styles sont obtenus très simplement par quelques caractères spéciaux:

```
Texte en **Gras** ou _Italique_ ou `Code`

# Titre 1
## Titre 2
### Titre 3

- Liste
- Non ordonnée

1. Liste
2. Numérotée

```

Il est aussi possible de créer des tableaux et bien d'autres éléments.
Plus d'info (en anglais) sur le [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

Quelques [astuces](tipstricks.md) pour mettre en page en utilisant Markdown

### Avec Atom

"code" crée un bloc de code
```
Du code dans ce bloc
```

"table" crée un tableau

| Header One     | Header Two     |
| :------------- | :------------- |
| Item One       | Item Two       |


De nombreux contributeurs ont créé des packages pour améliorer Atom, notamment sur le traitement du texte markdown.


https://atom.io/packages/markdown-writer

https://atom.io/packages/markdown-pdf
