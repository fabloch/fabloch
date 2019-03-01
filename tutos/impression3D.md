# Tuto impression 3D

## Introduction

Qu'est-ce que l'impression 3D ?
L’impression 3D est un procédé de fabrication additive, c’est à dire qu’on vient superposer des couches de matière pour réaliser une pièce en trois dimensions en partant d’un fichier STL (STereoLithography) généré par un logiciel de modélisation. L’origine de cette technologie remonte aux années 1980, le premier brevet commercial datant de 1986.

## Les différentes techniques d’impression

### Par dépôt de matière
La technique la plus répandue et utilisé au sein de La fabrique du Loch, est l’impresssion par dépôt de matière fondue:
	Appelée Fused deposition modeling (FDM), cette technique consiste à déposer par couches successives une matière (sous forme de filament) portée à température de fusion (liquide) dans une tête d’impression appelée extrudeur.

### Les autres techniques

#### Stéréolithographie (SLA)
Ce procédé  utilise comme matériau d’impression une résine liquide solidifiée sous l’effet d’une lumière UV.

#### Digital Light Processing (DLP)
Très similaire au SLA mais plus rapide et moins coûteux, ce procédé diffère par l'utilisation d'un projecteur à la place d'un rayon laser UV.
Ces deux techniques étant très proches, le procédé de fabrication est identique; l’objet fabriqué peut être tiré en dehors du photopolymère (résine) créant ainsi de l'espace au fond du réservoir pour la couche suivante, ou être plongé dans le réservoir afin de créer une nouvelle couche à sa surface.

#### Selective Laser Sintering (SLS) ou frittage sélectif par laser
Le frittage est un procédé de fabrication consistant à chauffer une poudre. Sous l’effet de la chaleur, les grains se soudent entre eux.
Comme pour les autres techniques, on procède couche par couche, un piston se chargeant de fournir la poudre et un rouleau se chargeant de l’étaler. C’est un laser de forte puissance qui chauffe la poudre ensuite. Cette technique permet d’utiliser une grande variété de matières dont des métaux (titane, acier et alliages) et des polymères.

#### Selective laser melting (SLM) ou fusion sélective par laser
La fusion sélective par laser, utilise un laser de haute puissance qui va faire fondre la poudre métallique de façon successive couche par couche.

#### Electron Beam Melting (EBM)
Tout comme la fusion sélective par laser, cette technologie d'impression procède par fusion de poudre de métal. La technique EBM a la particularité d’utiliser un faisceau d'électrons (à la place d'un laser) pour faire fondre la poudre de métal couche par couche.

## Les imprimantes 3D (FDM)

Composition d’une imprimante 3D

Le Plateau :

Le plateau est la surface sur laquelle les pièces sont imprimées, il peut être chauffant ou non pour aider à l’adhérence de la matière sur le plateau.

La tête d’impression (extrudeur):
La tête d’impression est la partie de la machine qui vient déposer la matière sur le plateau. Elle fonctionne comme suit :

Un moteur entraîne le filament dans un tube, au bout de ce tube se trouve une partie chauffante qui le fait fondre. La matière fondue est alors extrudée, par pression et par gravité, au travers d’une buse, une petite pièce percée à un diamètre spécifique. Le moteur peut aussi tirer le fil pour arrêter le flux lors des déplacements à vide.
L’extrudeur est aussi muni d’un ou plusieurs ventilateurs pour améliorer la maîtrise de la température d’impression. Ils servent à solidifier rapidement le plastique liquide.

Le contrôleur

Au cœur d’une imprimante 3D se trouve un petit ordinateur, il est le cerveau de l’imprimante et gère tous les mouvements de celle-ci.

Sur les imprimantes de “La fabrique du Loch” il s'agit d’un arduino 2560 couplé à une carte RAMP 1.4, le tout tournant sur le firmware libre Marlin. Il communique avec Repetier-Host via USB.

Arduino 2560

Imprimer une pièce

Processus 	
 A partir d’un dessin 3D ( en STL ou OBJ ) est d’abord découpé en tranche par Cura puis repetier en extrait un G.code qui commande les moteurs de l’imprimante.

Pour imprimer une pièce, encore faut-il avoir un modèle de cette pièce, plusieurs solutions s’offrent à vous.

Dessiner

Une première solution consiste à dessiner la pièce soi-même sur un logiciel de dessin 3D.
Plusieurs logiciel s’offrent à vous dont  :

	•	FreeCAD ( Gratuit et complet )
	•	Solidworks ( Payant )
	•	AutoCAD ( Payant )
	•	TinkerCAD ( Gratuit mais assez limité )

Une autre façon de se procurer un modèle 3D est de se rendre sur un site qui en propose. A la Fabrique, il est conseillé d’importer ses modèles en (.stl).  En voici quelques-un :

	•	thingiverse.com
	•	myminifactory.com
	•	yeggi.com
	•

Note : Lorsque vous récupérez des pièces sur Internet, regardez les conditions de partages mises en place par l’auteur.


Scanner

Enfin, “La Fabrique du Loch” possède un scanner 3D (Einscan-S). Il est possible de créer un modèle 3D à partir d’un objet réel en utilisant un scanner 3D.


## Les logiciels

### Repetier

Repetier-Host est un logiciel qui rassemble tous les outils nécessaires pour imprimer une pièce en 3D. Il permet de placer les objets où et comme on veut sur le plateau, de les trancher grâce à l’intégration d’un trancheur comme Cura ou Slic3r, et enfin d’envoyer la pièce à l’imprimante. Il permet aussi le contrôle manuel de l’imprimante : mouvements des axes, températures, refroidissements et autre, par une interface simple.

### Les Slicers

	On a vu que le principe de l’impression 3D est de déposer une matière couche après couche jusqu’à l’obtention de la pièce finale. Le programme qui gère cette phase de tranchage est appelé un slicer ou trancheur en français. Il analyse le modèle, le décompose en plusieurs tranches correspondant à chaque passe de dépôt de matière et génère un code que l’imprimante 3D saura interpréter: le G-code. Il existe de nombreux trancheurs, gratuits et payants, les plus connus étant Slic3r et CuraEngine, ce dernier étant celui utilisé à la Fabrique.


 “La fabrique du Loch”  utilise la version de CuraEngine intégrée dans Repetier-Host.

Trancher
/
Pour cette étape nous utiliserons Repetier-Host : 	


Charger sa pièce
La première chose à faire est de charger sa pièce dans Repetier, pour ce faire, cliquez sur le bouton “Charger” :

Sélectionnez votre pièce grâce à la fenêtre qui s’affiche.


Transformation de la pièce pour l’impression


Une fois la pièce chargée, il est possible de la manipuler grâce aux outils suivants :

Dans l’ordre :

	•	Sauvegarder
	•	Ajouter un objet
	•	Copier l’objet
	•	Positionner les objets automatiquement sur le plateau
	•	Centrer l’objet sur le plateau
	•	Changer l'échelle( la taille ) de l’objet
	•	Tourner l’objet
	•	Vue en tranche de l’objet
	•	En cliquant sur l’engrenage correspondant à la pièce dans la liste des objets vous pouvez avoir accès à ses propriétés, notamment la taille de l’objet affichée dans l’onglet analysé, sous le champ Taille. Vous pouvez aussi vous repérer grâce au quadrillage de l’aperçu qui vaut 1cm 2
Trancher l’objet

Il faut maintenant couper la pièce en tranche afin de montrer à la machine comment imprimer les différentes couches, nous allons diviser cette étape en deux sections, une première avec des réglages simples, et une seconde avec des réglages plus avancés.   

Configuration Simple

L’onglet de tranchage offre une suite de réglages :


Trancheur (manager)

	Permet de choisir le logiciel de tranchage. Cura est un bon choix pour la version simplifiée. Slic3r est une autre option qui possède des options légèrement différentes, nous aborderons cela plus loin dans ce tutoriel.

Configuration impression

	Permet de choisir un profil d’impression. Celui-ci est défini par 2 paramètres en particulier :
	Le premier se rapporte à la machine que vous utilisez. Sur celle-ci est renseigné un diamètre de buse. Le Fablab possède différentes buses allant de Ø2 à Ø5. Celles-ci étant un peu compliquée à changer il vaut mieux demander l’aide d’un manager ou choisir une machine équipée de la bonne buse. A noter que le Ø de la buse influe sur l’épaisseur des couches d’impression ( il faut 2 couches de Ø 0.2mm pour 1 couches de Ø 0,4mm ) et donc sur le temps d’impression (2 fois plus de couche)

Cependant on peut régler plus précisément l’épaisseur des couches, et c’est le second réglage. Au delà de la taille de la buse, il est possible « d’écraser » les couches les unes sur les autres en montant la buse d’une hauteur inférieurs à celle d’une couche « standard ».
Par ce biais les couches viendront s’empiler en compressant légèrement les couches précédentes, ce qui permet d’améliorer le rendu en faisant disparaître en partie l’espace entre les couches. Ce gain en précision entraîne comme expliqué plus haut un temps d’impression plus long.

A partir de ces deux paramètres choisissez un des profils pré-crées qui s’intitulent comme suit :
 Buse X (choisir le Ø de la buse installée) épaisseur X (renseigner la précision choisie)

Adhésion Type

	Ici, on choisit un type de structure pour aider la pièce à adhérer à la surface d’impression. Les choix sont :

	•	Aucun : Ceci n’est pas recommandé sauf si la pièce possède une grande surface en contact avec le plateau. Elle risque de se décoller si elle est haute.
	•
	•	Brim : Permets de créer une bordure autour de la pièce afin d'augmenter sa surface de contact avec le lit d’impression. Cette option permet aussi d’amorcer et de stabiliser le bon débit du filament avant d’attaquer l’impression de la pièce en elle-même.
	•	Raft : créer une plate-forme sous la pièce. Efficace pour des pièce n’ayant pas beaucoup d’emprise au sol (comme les pieds d’une figurine par exemple)


Indépendamment du type d’adhésion choisi il faut réfléchir à la manière de retirer ceux-ci à la fin de l’impression. Souvent le brim se retire facilement à la main. Le raft peut être plus compliqué dans le cas d’une pièce avec une base fine.

Qualité

Hauteur de couche de l’impression, un couche fine résultera en une pièce plus détaillée mais prendra plus de temps. Les hauteurs de couche disponibles dépendent du diamètre de la buse de l’imprimante. D’autre part ce réglage renvoie à l’épaisseur des couches choisies dans le profil d’impression et modifie ce dernier ( imprimer en buse 04 ep 03 avec une qualité de 0.2 revient à imprimer avec une buse 04 ep 02 ).

Support Type

Les support sont des structures qui viennent supporter les parties de la pièce en port-à-faux.

Trois choix sont disponible :
	•	Aucun : aucun support
	•	Contact avec le lit : créer des support seulement là ou la structure de support touchera le lit d’impression
	•	Partout : créer des support partout, même sur la pièce

Si aucun support n’apparaît après le tranchage malgré vos réglages, c’est que la machine ne juge pas nécessaire d’en réaliser.

Vitesse

Choix de la vitesse d’impression, les réglages fins de vitesses seront abordés dans la configuration avancée.

Densité de remplissage

De 0% pour une pièce creuse à 100% pour une pièce pleine.
Réduire la densité de remplissage permet d’économiser du temps d’impression et du filament. Nous recommandons entre 20 et 30 % de remplissages pour des pièces de décoration ou des figurines ou 80, 90 % pour des pièces nécessitant une résistance ou une rigidité (pièces mécaniques).



Configuration avancée

Pour accéder aux paramètres avancé, cliquez sur configuration sous l’option de trancheur.

Nous verrons ici les paramètres de configuration de Cura ( ces paramètres sont globalement les même dans d’autre trancheurs ).

Ils sont séparés en deux sections : Impression  et Filament.

Ces paramétrages peuvent être sauvegardés en profils, pour différents filaments et configurations d’imprimante.

Impression
Cette section traite des paramètres de vitesse, de qualité, de structure et d’extrusion :

Vitesses


Ces paramètres définissent les vitesses minimum et maximum des différentes phases de l’impression, ce sont ces valeurs qui seront prisent par le slicer (“Vitesse” dans la section tranchage de Repetier).

Comme on peut le voir, certaines couches disposent de réglages particuliers car elles demandent souvent une attention particulière, notamment la première couche et le périmètre extérieur qui prennent souvent plus de temps pour construire des bases solides.

	D’autre part il est possible d’agir sur les vitesses durant l’impression via le panneau de contrôle manuel. Ces méthodes demandent un peu de pratique pour ne pas ruiner votre impression. Si votre pièce comporte une couche compliquée ou si vous voyez que le filament à du mal à adhérer aux couches inférieurs, vous pouvez réduire la vitesse.
D’un autre coté si vous attaquez une deuxième épaisseur en plein qui vise à fermer le dessus de la pièce on peut accélérer un peu la vitesse.



Qualité

Ici sont définies les différentes hauteurs de couche disponible dans ce profil.
La hauteur et la largeur de la première couche jouent sur l’adhésion de la pièce sur le plateau.

Remplissage


Les paramètres de remplissage concernent les parois et l'intérieur de la pièce à imprimer.
	•	Épaisseur parois : épaisseur en mm de la paroi de la pièce ( préférer un multiple du diamètre de buse  (ex : 0.6 pour une buse de 0.3 pour une paroi de 2 couches ).
	•	Épaisseur Base/Sommet : épaisseur des paroi inférieurs et supérieurs de la pièce.
	•	Valeur Recouvrement : taux de chevauchement entre le motif de remplissage et les parois.
	•	Remplissage Motif : choix du motif de remplissage, plusieurs possibilités :
	◦	Automatique
	◦	Grid :
	▪
	◦

	◦	Lignes
	▪
	▪
	◦	Lignes Concentriques
	◦
	▪
Support

Cette partie permet de régler les options des supports :

	•	Modèle de Support : Grid ou Lignes, même motifs que pour le remplissage de la pièce.
	•	Surplomb Angle : défini à partir de quel angle avec le plateau la pièce doit être pour que des supports soit générés. ( n’affecte que le support de type ).
	•	Valeur de remplissage : densité de remplissage des supports.
	•	Distance X/Y : a quelle distance de la pièce les supports sont générés sur les axes X/Y; facilite le retrait des supports après l’impression.
	•	Distance X/Y : même chose pour l’axe Z.

Skirt and Brim

Skirt (jupe) et Brim(bordure) sont des solutions pour l’adhésion de la pièce au lit d’impression :

Skirt : périmètre imprimé autour de la pièce permettant de préparer la buse a l’impression.

Brim : bordure imprimée autour de la base de la pièce, elle augmente la surface de contacte entre la pièce et le plateau d’impression.
	•	Nb lignes de Contour : Le nombre de lignes effectuées autour de la pièce.
	•	Contour distance : La distance entre la pièce et la jupe.
	•	Longueur minimum de purge : longueur minimum de la jupe afin de purger la buse.
	•	Brim Largeur : largeur du brim.

Raft


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


Paramètre générale extrudeur


	•	Spiralizer Contour( mode vase ) : imprimer la pièce en une longue spirale continue
	◦	Toutes les pièces ne sont pas imprimable dans ce mode
	◦	Les parois auront une seul épaisseur car un seul passage de la buse
	•	Activer rétraction :
Sans rétractation, la matière continue à se déposer pendant que la tête se déplace vers son nouveau point d’impression. En activant cette option, la buse va aspirer l’excédent de matière, évitant ainsi des dépôts indésirables sur le parcours de la tête d’impression en améliorant le rendu final.
	•	Périmètre avant remplissage : pour chaque couche, les parois sont imprimées avant le remplissage.
	•	Vitesse rétraction : la vitesse de rétraction du filament.
	•	Distance rétraction : la distance de rétraction du filament.
	•	Déplacement minimum avant rétraction : distance de déplacement minimum pour activer la rétraction.
	•	Extrusion minimale avant rétraction : quantité minimum d’extrusion avant la prochaine rétraction.
	•	Z Relevage : la tête d’impression est relevé pendant la rétraction.
	•	Couper l’objet en bas : commence l’impression à une couche avancée du modèle (ignore les couches inférieures)  
	•	Diamètre buse : le diamètre de la buse sur la machine.
	•	Minimiser croisement périmètre : essai de déplacer la tête d’impression dans la pièce afin d’éviter les fils de liaison.











Imprimer

On peut lancer la chauffe de la machine avant les réglages pour gagner du temps sur le temps de chauffe de la machine.

	1.	Connecter l’imprimante  

Établir le lien avec l’imprimante à l’aide du bouton :


	1.	Mettre imprimante en chauffe

     Il faut ensuite faire chauffer la buse et le plateau
grâce aux boutons suivants, cliquer dessus lance la chauffe des éléments jusqu’au seuil renseigné dans les réglages.
On peut surveiller celle-ci via le curseur en forme de losange qui doit atteindre le seuil décidé au préalable


	1.	Lancer l’impression

Une fois les éléments à température adéquates il reste juste à lancer le travail via le bouton :
L’imprimante se déplace alors à son point de départ et démarre l’impression.


	1.	Moucher la buse avant impression

Avant qu’elle ne démarre le travail il est préférable de retirer le trop plein de matière à la sortie de la buse afin qu’elle n’interfère pas avec l’impression.






















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


















Différents matériaux utilisables :

La fabrique du loch dispose de plusieurs matériaux différents. Ces filaments « spéciaux » nécessitent souvent des réglages particuliers et ne sont proposés que dans des cas particuliers et leur utilisation peut provoquer un surcoût.
Voilà une liste des autres matériaux :

PLA :

C’est le plastique de base de la Fabrique, biodégradable (à base d’amidon de maïs) il est disponible en diverses couleurs. Il est facile à imprimer. Sa résistance est néanmoins limité (biodégradable) et il n’est pas recommandé pour des pièces destinées à l’extérieur ou une exposition à l’eau

. Température de fusion :  205°C
Température plateau : de 0 à 55°C  



ABS :
 Lissage à l'acétone
	Plus souple et plus résistant aux choc, à l’eau et aux UV, c’est le plastique phare de l’industrie par exemple des Lego. Il diffuse cependant des émission de particules fines lors de la fusion.  
	Sur un plan plus pratique l’impression en ABS nécessite souvent une précaution particulière vis à vis de l’homogénéité thermique. Il est aussi recommandé de produire un badigeon (d’ABS et d’acétone) à déposer au préalable sur le plateau pour améliorer l’adhérence.

Il peut cependant être lissé via des techniques de chimie pour une meilleure finition.

Température de fusion ( ~250°C )
Température plateau ( ~ 70°C )

 Exemple d'impression en fibre de bois

	Nous disposons aussi de quelques échantillons de PLA enrichi avec des fibres. Celle-ci permettent d’améliorer les caractéristique de ce derniers et son rendu. Tous ces matériaux demandent une précaution particulière dans le nettoyage de la machine. Les fibres ont tendance à se déposer et boucher la buse.
	Nous disposons entre autres de fibre de carbone. Ce matériau permet une résistance mécanique optimale pour un poids minimal.

Les fibres de Bronze permettent d’avoir une pièce un peu plus solide mais surtout plus lourde le rendu est aussi un peu particulier.
Les fibres de bois donnent aussi un autre type de rendu.

	Étant réalisé à base de fibres, réparties de manière plus ou moins homogène, les résultats sont assez variables.

FLEX :

Comme son nom le laisse présumer, ceci est un matériau flexible. Efficace pour imprimer des objets nécessitant un peu d’élasticité (courroie, roue, patins… ) , ce matériau est un peu plus compliqué à imprimer que le PLA.

Température de fusion :  250°C
température plateau : 90° C
