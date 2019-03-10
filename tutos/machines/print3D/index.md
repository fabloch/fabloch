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

## Préparer l'objet

- [Imprimer](imprimer)
- [Trancher](trancher)
- [Configurer](configurer)

## Imprimer

- Moucher la buse avant impression

	Avant qu’elle ne démarre le travail il est préférable de retirer le trop plein de matière à la sortie de la buse afin qu’elle n’interfère pas avec l’impression.

- Lancer l’impression

	Une fois les éléments à température adéquates il reste juste à lancer le travail via le bouton :
	L’imprimante se déplace alors à son point de départ et démarre l’impression.






















Contrôles manuels :

Il est possible d’interagir avec le machine manuellement et ce même durant la phase d’impression. Même si cela n’est pas recommandé la plupart du temps, cela permets de faire diverses actions dont le changement de bobine.

Déplacement en X (gauche droite)  et Y (haut et bas)
Origine machine en X/Y/Z  ou origine absolue
Déroulement du fil
(débit ou rétractation)
Déplacement en Z










Paramètre de vitesse



Température de chauffe plateau et buse



















Vous pouvez aussi mettre en pause ou arrêter l’impression grâce aux boutons situés dans la barre d’outils à gauche.













Changement et réglages du filament

Changement de bobine :

	Pour changer de bobine rien de plus simple. Après avoir connecté votre imprimante vous devez chauffer la buse pour pouvoir extraire le filament. récupérez ensuite la cale ( cachée dans le rail en bas à gauche de l’imprimante ! ) puis positionnez-là dans l’espace derrière le filament.
	Regardez ensuite du coté du panneau de contrôle manuel et lancez une rétractation du filament de 100 mm (dernier cadran vers le haut) lorsque le fil est sorti, vous pouvez ranger la bobine et installer la nouvelle après avoir taillé le bout en pointe pour en faciliter l’insertion. Placez le bout du fil au fond du trou et, en le maintenant, appuyez sur le bouton de déroulement puissance 100mm (le même qu’avant mais vers le bas cette fois). Lorsque la cale n’est plus maintenue, le filament est bien enclenché. Attendez de le voir apparaître à la sortie de la buse et relancez une descente du fil si nécessaire. Il ne vous reste qu’à « moucher » la buse pour repartir d’une base propre et vous pouvez y aller.
