# Github pages

Il est possible de configurer certains paramètres de Jekyll:
[Configuration de Jekyll](https://help.github.com/articles/configuring-jekyll/)

[Configuration de FrontMatter](https://jekyllrb.com/docs/front-matter/)

Il est ainsi possible de créer des variables spécifiques par page.
```
---
food: Pizza
---

<h1>{{ page.food }}</h1>
```
