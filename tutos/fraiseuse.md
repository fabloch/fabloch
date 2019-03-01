# Tuto fraiseuse

note : version sans illustrations


1.Introduction 
1.1 le fraisage
 Le fraisage est une technique alliant d'une part la rotation de la fraise et d'autre part le déplacement de la pièce brut dans le but de produire une réalisation (gravure, pièce...). Elle est effectué à l'aide d'un outil spécial, la fraiseuse, dans notre cas, la SRM-20 de chez Roland.

  1.2 les différentes têtes
 En fonction de l'opération que vous souhaitez effectuer, différentes tête seront à privilégier. <reprendre la page du manuel dessus> Cependant, la Fabrique ne dispose que de têtes plates, ce tuto se concentrera donc uniquement sur leur utilisation

1.3 caractéristiques

la SRM-20 vous permet d'utiliser des matériau brut d'environs 20*15cm, avec une hauteur pouvant varier entre les deux positions de mandrin possibles. En position basse, comptez une hauteur d'environs 4cm, contre 7 en position haute.  1.4 les différents matériaux
 Plus de tests sont nécessaies  

2. face simple

 2.1 liste des logiciels et sites utilisés dans ce tuto

Tinkercad : modélisation 3D Vpannel : configuration et gestion de la machine
Modula Player : configuration et gestion des découpes  2.2 Préparer la machine
 Placez votre matériau de base dans la machine et fixez là à l'aide de scotch double face et du dispositif déjà en place.  Allumez la machine en appuyant sur le bouton on/off situé sur le dessus de la machine. Ouvrez Vpannel, sélectionnez user coordinate système.  Mettez la tête correspondant au travail que vous comptez faire.  Mise en place de l'origine utilisateur : à l'aide des boutons présents sur le logiciel, positionnez la fraise à l'origine que vous comptez utiliser, pour cela nous conseillons de se positionner sur l'un des quatres coins de votre pièce (de préférence le coin inférieur gauche) puis cliquez sur «X/Y » à droite, sous « set origin point ». abaissez ensuite la fraise, attention, le logiciel est par défaut en continue, utilisez les déplacement « x100 » « x10 » ou « x1 » dès que vous vous approchez de votre pièce faites tourner la fraise à l'aide du bouton « ON » sous « spindel » et abaissez en pas à pas (de préfèrence en x10) de telle sorte à ce que la fraise touche tout juste la surface de votre pièce, puis stopper la rotation de la fraise (OFF sous spindel) et cliquez sur « Z » à droite, sous « set origin point ».  2.3 modélisation de la pièce
Pour modéliser votre pièce, vous pouvez utiliser le site « tinkercad », faite une boite aux dimensions de votre pièce brut, et appliquez-y les perçages correspondant au travail que vous souhaitez effetcuer. Il est à noter qu'au moment de lancer les opérations à effectuer sur la pièce, la machine ne creusera pas plus profondément que ce qui est indiqué sur le modèle 3D mais pourra creuser moins profondément, ainsi avec un creux d'1cm pourra servir pour un creux de 5mm mais pas pour un creux d'1.5cm. Une fois la modélisation terminée, exporter votre objet 3D en .stl  2.4 préparer les travaux Vous pouvez désormais lancer Modela Player et y ouvrir votre modèle 3D précédement exporté.  Une fois ceci fait, allez dans les options du modèle (bouton boussole à droite à côté de « matériau »), puis dans « origine » et cliquez sur l'origine correspondant à celle réglée sur la machine (ici, le coin inférieur gauche).  Maintenant, vous allez pouvoir cliquer sur « nouveau processus » pour lancer un nouveau travail, voyons chaque écran un par un.  « choisir le type de processus »
comme vous le voyez, vous avez le choix entre 4 types de processus
surfaçage
Fait un passage sur votre matériau afin de mettre sa surface à niveau pour l'uniformiser
dégrossissage
Sert à faire une première passe pour avoir déjà une forme brute de votre résultat final
finition
Seconde passe plus précise afin de lisser le dégrossissage avant de récupérer votre pièce
forage
Permet de percer un trou au travers de votre matériau
 Séléctionner la surface de coupe :
nous reviendrons dessus sur le chapitre « le fraisage sur faces multiples ».   « choisir l'outil » Assurez vous de sélectionner l'outil installé dans la machine à l'aide du menu déroulant.  « régler l'aire et la profondeur » Si votre modèle 3D correspond déjà exactement à ce que vous souhaitez faire et qu'un seul outil vous est nécessaire, cochez « tout » et cliquez sur suivant.  Sinon, cochez « en partie », vous pourrez alors recadrer la surface d'action à gauche à l'aide des outils suivants 
Icône curseur
Redimensionner le cadre à l'aide des carré dans les coins supérieur droit et inférieur gauche. Déplacer le cadre en cliquant à l'intérieur.
Icône fleches
Déplacer le modèle
Icône loupe
Zoomer sur le modèle
Icône dézoom
Afficher l'intégralité du modèle
 Vous pourrez également choisir la profondeur, où 0 correspondant à votre origine machine Z (normalement, la surface de votre matériau) et une valeur négative correspond à un creux dans votre matériau.  « choisir le type de trajectoire d'outil »
Vous pouvez maintenant choisir le mouvement fait par votre outil lors de ectte opération.  
Lignes de ballayage
Votre outil effectuera des aller-retours le long de votre aire de travail. X : les aller-retours se feront le long de l'axe X (longeur) Y : les aller-retours se feront le long de l'axe Y (largeur) X/Y : un premier passage se fera le long de l'axe X, puis un second passage se fera le long de l'axe Y.
Unidirrectionnelles
Votre outil effectuera une ligne droite avant de revenir juste a côté de son point de départ, cela tout le long de votre aire de travail  X : les lignes s'effectuent le long de l'axe X (longueur) Y : les lignes s'effectuent le long de l'axe Y (largeur)
Lignes de contour
L'outil va suivre les contours de la/des forme(s) présentent dans l'air de travail, sans s'occuper de l'intérieur.
Spirales
(finition seulement) l'outil va effectuer des tours sur l'aire de travail, se rapprochant progressivement du centre.
« Régler les paramètres de coupe » :
Cet écran vous permet de régler les détails de la découpe, il est préférable de laisser ces options par défaut.  « entrer un nom » Enfin cet écran, assez explicite, vous invite à nommer votre processus et à le faire calculer soit immédiatement soit ultérieurement. 
2.5 lancer les travaux Une fois tous vos travaux prêts, cliquer sur le bouton « usiner », un écran s'ouvrira enfin, vous permettant d'exporter les travaux sous forme de fichier .prn, contenant un G-Code Roland compatible avec la machine, pour une utilisation ultérieure. Vous pouvez également laisser l'option « sortie vers fichier » décochée afin de lancer le travail directement. Pensez à ouvrir Vpannel afin de régler des détails que vous n'avez peut-être pas prit en compte précédemment (mauvaise vitesse de déplacement/rotation par exemple) ainsi que pour mettre la machine en pause voir annuler le travail en cours en cas de besoin.  2.6 nettoyer la machine. Une fois vos travaux terminer, retirer votre matériau et pensez à au moins passer l'aspirateur à l'intérieur de la machine afin de retirer tout copeau et poussière.
