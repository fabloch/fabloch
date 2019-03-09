# Le mode d'emploi de la découpeuse laser

## Inkcape
- Etape 1: [Editer son fichier .svg avec Inkscape](inkscape.md)

Nous avons maintenant un fichier au format .SVG propre pour être traité par la découpeuse laser. Il faut maintenant paramétrer la découpeuse pour traiter ce fichier correctement.

## Visicut

[Visicut pour la découpe laser](https://www.lafabriqueduloch.org/projet/visicut-decoupe-laser/)

Visicut permet d’associer aux éléments du dessin vectoriel (fichier .SVG) un ensemble d’actions (découpe, marquage ou gravure). La chaîne est la suivante :

![Laser](images/laser7.png)

- Etape 2: [Mapper les objets avec Visicut](mapping)
- Etape 2 bis: [Définir les paramètres laser pour les objets](profiles)

Nous avons maintenant un fichier au format .PLF

- Etape 3: [Définition des paramètres Vitesse / Puissance du laser](vitesse-puissance)
- Etape 4: [Générer le gcode avec Visicut](gcode)

Nous avons maintenant un fichier au format .GCODE que l'on peut envoyer à la découpeuse laser.

Il est temps de placer la matière à découper et de régler la machine.

## Octoprint
- Etape 5: [Contrôler la progression du travail](octoprint)
