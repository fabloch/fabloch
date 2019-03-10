## Les imprimantes 3D (FDM)

Composition d’une imprimante 3D

### Le Plateau

Le plateau est la surface sur laquelle les pièces sont imprimées, il peut être chauffant ou non pour aider à l’adhérence de la matière sur le plateau.

### La tête d’impression (extrudeur)
La tête d’impression est la partie de la machine qui vient déposer la matière sur le plateau. Elle fonctionne comme suit :

Un moteur entraîne le filament dans un tube, au bout de ce tube se trouve une partie chauffante qui le fait fondre. La matière fondue est alors extrudée, par pression et par gravité, au travers d’une buse, une petite pièce percée à un diamètre spécifique. Le moteur peut aussi tirer le fil pour arrêter le flux lors des déplacements à vide.
L’extrudeur est aussi muni d’un ou plusieurs ventilateurs pour améliorer la maîtrise de la température d’impression. Ils servent à solidifier rapidement le plastique liquide.

### Le contrôleur

Au cœur d’une imprimante 3D se trouve un petit ordinateur, il est le cerveau de l’imprimante et gère tous les mouvements de celle-ci.

Sur les imprimantes de “La fabrique du Loch” il s'agit d’un arduino 2560 couplé à une carte RAMP 1.4, le tout tournant sur le firmware libre Marlin. Il communique avec Repetier-Host via USB.

Arduino 2560
