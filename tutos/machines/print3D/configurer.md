# Configuration impression

Permet de choisir un profil d’impression.

Celui-ci est défini par 2 paramètres en particulier :
- Le premier se rapporte à la machine que vous utilisez, le diamètre de la buse

Sur celle-ci est renseigné un diamètre de buse. Le Fablab possède différentes buses allant de Ø2 à Ø5. Celles-ci étant un peu compliquée à changer il vaut mieux demander l’aide d’un manager ou choisir une machine équipée de la bonne buse.

A noter que le Ø de la buse influe sur l’épaisseur des couches d’impression ( il faut 2 couches de Ø 0.2mm pour 1 couches de Ø 0,4mm ) et donc sur le temps d’impression (2 fois plus de couche)

- le second est l'écrasement des couches
Cependant on peut régler plus précisément l’épaisseur des couches, et c’est le second réglage. Au delà de la taille de la buse, il est possible « d’écraser » les couches les unes sur les autres en montant la buse d’une hauteur inférieurs à celle d’une couche « standard ».

Par ce biais les couches viendront s’empiler en compressant légèrement les couches précédentes, ce qui permet d’améliorer le rendu en faisant disparaître en partie l’espace entre les couches. Ce gain en précision entraîne comme expliqué plus haut un temps d’impression plus long.

A partir de ces deux paramètres choisissez un des profils pré-créés qui s’intitulent comme suit :
```
 Buse X (choisir le Ø de la buse installée) épaisseur X (renseigner la précision choisie)
```

## Adhésion Type

Ici, on choisit un type de structure pour aider la pièce à adhérer à la surface d’impression. Les choix sont :

	•	Aucun : Ceci n’est pas recommandé sauf si la pièce possède une grande surface en contact avec le plateau. Elle risque de se décoller si elle est haute.
	•
	•	Brim : Permets de créer une bordure autour de la pièce afin d'augmenter sa surface de contact avec le lit d’impression. Cette option permet aussi d’amorcer et de stabiliser le bon débit du filament avant d’attaquer l’impression de la pièce en elle-même.
	•	Raft : créer une plate-forme sous la pièce. Efficace pour des pièce n’ayant pas beaucoup d’emprise au sol (comme les pieds d’une figurine par exemple)


Indépendamment du type d’adhésion choisi il faut réfléchir à la manière de retirer ceux-ci à la fin de l’impression. Souvent le brim se retire facilement à la main. Le raft peut être plus compliqué dans le cas d’une pièce avec une base fine.

## Qualité

Hauteur de couche de l’impression, un couche fine résultera en une pièce plus détaillée mais prendra plus de temps. Les hauteurs de couche disponibles dépendent du diamètre de la buse de l’imprimante. D’autre part ce réglage renvoie à l’épaisseur des couches choisies dans le profil d’impression et modifie ce dernier ( imprimer en buse 04 ep 03 avec une qualité de 0.2 revient à imprimer avec une buse 04 ep 02 ).

## Support Type

Les support sont des structures qui viennent supporter les parties de la pièce en port-à-faux.

Trois choix sont disponible :
	•	Aucun : aucun support
	•	Contact avec le lit : créer des support seulement là ou la structure de support touchera le lit d’impression
	•	Partout : créer des support partout, même sur la pièce

Si aucun support n’apparaît après le tranchage malgré vos réglages, c’est que la machine ne juge pas nécessaire d’en réaliser.

## Vitesse

Choix de la vitesse d’impression, les réglages fins de vitesses seront abordés dans la configuration avancée.

## Densité de remplissage

De 0% pour une pièce creuse à 100% pour une pièce pleine.
Réduire la densité de remplissage permet d’économiser du temps d’impression et du filament. Nous recommandons entre 20 et 30 % de remplissages pour des pièces de décoration ou des figurines ou 80, 90 % pour des pièces nécessitant une résistance ou une rigidité (pièces mécaniques).
