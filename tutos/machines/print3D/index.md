# Tuto impression 3D

## Qu'est-ce que l'impression 3D ?

L’impression 3D est un procédé de fabrication additive, c’est à dire qu’on vient superposer des couches de matière pour réaliser une pièce en trois dimensions en partant d’un fichier STL (STereoLithography) généré par un logiciel de modélisation. L’origine de cette technologie remonte aux années 1980, le premier brevet commercial datant de 1986.

[Les différentes techniques d'impression](techniques)
[Les imprimantes 3D (FDM)](imprimantes)
[Logiciels](logiciels)

## Processus 	

Un dessin 3D ( en STL ou OBJ ) est d’abord découpé en tranche par Cura puis repetier pour produire des instructions .gcode qui commande les moteurs de l’imprimante.

## Préparer l'imprimante
On peut lancer la chauffe de la machine avant les réglages pour gagner du temps sur le temps de chauffe de la machine.

```
	Connecter l’imprimante  
```

Établir le lien avec l’imprimante à l’aide du bouton :

```
	Mettre imprimante en chauffe
```

Il faut ensuite faire chauffer la buse et le plateau grâce aux boutons suivants, cliquer dessus lance la chauffe des éléments jusqu’au seuil renseigné dans les réglages.
On peut surveiller celle-ci via le curseur en forme de losange qui doit atteindre le seuil décidé au préalable

## Préparer la pièce

- [Concevoir une pièce](concevoir)
- [Trancher avec RepetierHost](trancher)
- [Configurer](configurer)

## Imprimer

- Moucher la buse avant impression

	Avant qu’elle ne démarre le travail, il est préférable de retirer le trop plein de matière à la sortie de la buse afin qu’elle n’interfère pas avec l’impression.

- Lancer l’impression

Une fois les éléments à température adéquates il reste à lancer le travail via le bouton :

L’imprimante se déplace alors à son point de départ et démarre l’impression.

- [Contrôles manuels pendant l'impression](controlesmanuels)
- [Changement de bobine](bobine)
