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

[Lien](url)

![Image](src)
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
