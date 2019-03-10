# Configuration avancée

Pour accéder aux paramètres avancé, cliquez sur configuration sous l’option de trancheur.

Nous verrons ici les paramètres de configuration de Cura ( ces paramètres sont globalement les même dans d’autre trancheurs ).

Ils sont séparés en deux sections : Impression  et Filament.

Ces paramétrages peuvent être sauvegardés en profils, pour différents filaments et configurations d’imprimante.

# Impression
Cette section traite des paramètres de vitesse, de qualité, de structure et d’extrusion :

## Vitesses

Ces paramètres définissent les vitesses minimum et maximum des différentes phases de l’impression, ce sont ces valeurs qui seront prisent par le slicer (“Vitesse” dans la section tranchage de Repetier).

Comme on peut le voir, certaines couches disposent de réglages particuliers car elles demandent souvent une attention particulière, notamment la première couche et le périmètre extérieur qui prennent souvent plus de temps pour construire des bases solides.

	D’autre part il est possible d’agir sur les vitesses durant l’impression via le panneau de contrôle manuel. Ces méthodes demandent un peu de pratique pour ne pas ruiner votre impression. Si votre pièce comporte une couche compliquée ou si vous voyez que le filament à du mal à adhérer aux couches inférieurs, vous pouvez réduire la vitesse.
D’un autre coté si vous attaquez une deuxième épaisseur en plein qui vise à fermer le dessus de la pièce on peut accélérer un peu la vitesse.

## Qualité

Ici sont définies les différentes hauteurs de couche disponible dans ce profil.
La hauteur et la largeur de la première couche jouent sur l’adhésion de la pièce sur le plateau.

## Remplissage

Les paramètres de remplissage concernent les parois et l'intérieur de la pièce à imprimer.
	•	Épaisseur parois : épaisseur en mm de la paroi de la pièce ( préférer un multiple du diamètre de buse  (ex : 0.6 pour une buse de 0.3 pour une paroi de 2 couches ).
	•	Épaisseur Base/Sommet : épaisseur des paroi inférieurs et supérieurs de la pièce.
	•	Valeur Recouvrement : taux de chevauchement entre le motif de remplissage et les parois.
	•	Remplissage Motif : choix du motif de remplissage, plusieurs possibilités :
	◦	Automatique
	◦	Grid :
	◦	Lignes
	◦	Lignes Concentriques

## Support

Cette partie permet de régler les options des supports :

	•	Modèle de Support : Grid ou Lignes, même motifs que pour le remplissage de la pièce.
	•	Surplomb Angle : défini à partir de quel angle avec le plateau la pièce doit être pour que des supports soit générés. ( n’affecte que le support de type ).
	•	Valeur de remplissage : densité de remplissage des supports.
	•	Distance X/Y : a quelle distance de la pièce les supports sont générés sur les axes X/Y; facilite le retrait des supports après l’impression.
	•	Distance X/Y : même chose pour l’axe Z.

### Skirt and Brim

Skirt (jupe) et Brim(bordure) sont des solutions pour l’adhésion de la pièce au lit d’impression :

#### Skirt
périmètre imprimé autour de la pièce permettant de préparer la buse a l’impression.

#### Brim
bordure imprimée autour de la base de la pièce, elle augmente la surface de contacte entre la pièce et le plateau d’impression.
	•	Nb lignes de Contour : Le nombre de lignes effectuées autour de la pièce.
	•	Contour distance : La distance entre la pièce et la jupe.
	•	Longueur minimum de purge : longueur minimum de la jupe afin de purger la buse.
	•	Brim Largeur : largeur du brim.

### Raft

Le raft( radeau ) est un autre type de structure en treillis visant à améliorer l’adhésion de la pièce au lit d’impression, il s'agit d’un « radeau » sur lequel la pièce sera imprimée. Il se compose comme suit :


	•
	•	Extra Marge : la largeur du raft autour de la pièce
	•	Épaisseur de la ligne de base : la ligne de base est souvent plus épaisse et écrasée contre le plateau, elle prend du temps à s’imprimer pour poser des fondations solides.
	•	Épaisseur Interface : la hauteur entre les différentes parties du raft (voir schéma)
	•	Air Gap Layer 0 : la distance entre le plateau et le raft.
	•	Air Gap : la distance entre le raft et la pièce : 0,1 mm paraît une bonne distance pour décoller le gap simplement tout en conservant l’utilité du raft.
	•	Espace Ligne : espace entre les lignes de la base du raft
	•	Largeur ligne base : la distance entre les lignes de bases.
	•	Épaisseur ligne interface : épaisseur des lignes du milieu.
	•	Nomb. couche surface : Le nombre de couche pleine au dessus du raft pour une bonne stabilité 2/3 couches recommandées.
