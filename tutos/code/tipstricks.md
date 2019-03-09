# Trucs et astuces Markdown
Pour jouer sur la taille d'une image:
```
![test image size](/assets/images/juju-NB.jpg){:class="img-responsive"}
![test image size](/assets/images/juju-NB.jpg){:height="50%" width="50%"}
![test image size](/assets/images/juju-NB.jpg){:height="700px" width="400px"}
```

Pour remplacer des liens provenant d'un fichier html
```
En utilisant votre éditeur de texte, demander une recherche par expression régulière
<a href="([^"]*)">([^<]*)</a>

Puis appliquer le remplacement par
[$2]($1)
```

Pour créer une ancre locale dans une longue page
https://gist.github.com/asabaylus/3071099
