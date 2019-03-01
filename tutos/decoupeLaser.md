# DÉCOUPEUSE LASER DE LA FABRIQUE DU LOCH
 
Caractéristiques techniques :

A la FABrique, on utilise majoritairement :
- Inkscape : dessin vectoriel (fichier au format .SVG)
- Visicut : association des dessins aux modes de découpe/marquage/gravure (fichier au format .PLF), définition des paramètres laser (DPI, Vitesse, Puissance), génération du G-CODE (fichier au format .GCODE)
- Octoprint estimation du temps d’exécution, envoi du G-CODE vers la découpe Laser,  suivi du travail (caméra)

## Usages
  "https://www.lafabriqueduloch.org/projet/usages-decoupe-laser/"https://www.lafabriqueduloch.org/projet/usages-decoupe-laser/

### Découpe vectorielle (cutting)
Le laser se déplace le long d’une ligne (courbe) relativement lentement, à puissance conséquente, ce qui a pour effet de découper le long du chemin.  Pour graver plusieurs motifs, les seuls déplacements non efficaces sont donc ceux permettant de passer d’un motif à un autre, laser OFF (et peu nombreux).

### Gravure vectorielle (marking)
Même principe que pour la découpe vectorielle, mais à des puissances plus faibles et des vitesses plus rapides, ne permettant pas au laser de découper la totalité de l‘épaisseur du matériau, mais seulement d’en retirer une partie : le contour est ainsi gravé.

Source : http://rowmark.com/MARK/laser_guide/pages/intro.asp

### Gravure RASTER (aplat - engraving)
A partir d’une image, ce procédé permet :
1. De transformer les couleurs de l’image en nuages de points noirs et de points blancs, dont la densité rend compte de la couleur (vu « de loin », l’espacement des points noirs donne une impression de nuance de gris). Plusieurs algorithmes sont envisageables (Floyd-Steinberg, Half Tone,  dithering…).
2. Le laser parcourt l’ensemble des pixels de l’image ainsi transformée, et brûle les pixels noirs en laissant intact les blancs. Il est à noter que tous les pixels noirs sont brûlés avec la même puissance dans ce mode RASTER. C’est uniquement leur espacement qui rendra compte d’une nuance de gris.

Sur cet exemple, le contour, les textes « conçu et réalisé à » et « Auray-Morbihan Bretagne » sont gravés en vectoriel, et le logo en raster. On voit la couverture de la zone à traitée, qu’il y ait des pixels à graver (noir) ou non (blanc). Ce procédé est coûteux en temps.

### Gravure Raster 3D (3D engraving)
Cette fois, l’image couleur est convertie en nuances de gris, et les pixels noirs seront gravés avec une puissance 100%, les blancs avec une puissance nulle, et les nuances de gris avec une puissance qui lui est proportionnelle. La puissance du laser est donc modulée en fonction de la valeur du pixel au-dessus duquel il se trouve, permettant de graver plus ou moins profondément le matériau, d’où une gravure RASTER 3D.


# INKSCAPE ET FICHIER .SVG.
On se référera au contenu de la formation proposée à la FABrique.

Problème d'échelle entre illustrator et Inkscape :
Format .SVG Illustrator et .SVG Inkscape
Les fichiers .SVG sont sauvegardés avec des unités en pixels, cependant inkscape et illustrator utilisent des facteurs de conversion px/mm différents :
illustrator 	72dpi : 72 px = 1 inch = 25.4 mm
inkscape 	90dpi : 90 px = 1 inch = 25.4 mm
Exemple
Supposons avoir créé un carré de côté 25.4mm dans Illustrator, lorsque vous enregistrez le fichier .SVG avec Illustrator, les dimensions sont converties en pixels  avec le ratio 72dpi : on a donc un carré de côté 72 pixels.
En l’ouvrant dans inkscape (export .svg), il ouvre un fichier contenant un carré de 72 pixels, en utilisant un ratio de 90dpi pour retrouver les dimensions de l’objet. On obtient donc un carré de côté 72px/90dpi = 0.8 inch = 20.32mm.

Il est donc nécessaire dans Inkscape de redimensionner les objets créés avec Illustrator d’un facteur de 90/72 = 125% afin de conserver les dimensions originales (en mm).
Redimensionner les SVG Illustrator d’un facteur 125% dans Inkscape
ouvrir le .SVG créé par Illustrator dans Inkscape
tout sélectionner (Ctrl+A), grouper (Ctrl+G).
dans le menu objet, transformer (Ctrl+Maj+M)
dans la nouvelle fenêtre, onglet mise a l’échelle : 125% (largeur et hauteur)
vérifier que les dimensions sont maintenant correctes.

Envoi du .SVG vers Visicut
Une fois le dessin terminé, l’ouvrir avec Visicut permettra de générer le G-CODE correspondant à la découpe/gravure Laser que l’on souhaite.
Sélectionner l’objet à découper ou à graver.
Menu Extension, LasercutPath, Open in Visicut


VISICUT

  "https://www.lafabriqueduloch.org/projet/visicut-decoupe-laser/"https://www.lafabriqueduloch.org/projet/visicut-decoupe-laser/

Visicut permet d’associer aux éléments du dessin vectoriel (fichier .SVG) un ensemble d’actions (découpe, marquage ou gravure). La chaîne est la suivante :

Mapping objets – profils laser
Cette étape va permettre de partitionner les objets contenus dans le dessin vectoriel, et de leur associer une action à réaliser.

Fichier .SVG dans Inkscape

Ouverture dans Visicut

Onglet Mapping

One profile for everything : le même profil laser pour tous les objets
Map by single property : on partitionne les objets pour les regrouper selon leurs caractéristiques, et affecter un profil laser spécifique
Stroke color : couleur du contours. Par exemple, découpe laser pour le rouge, marquage pour le bleu etc…
Fill color : couleur de remplissage
Layer : par calque
Stroke width : épaisseur de contours
Advanced mapping : utilisation avancée.
Profils laser

Cette étape va permettre de partitionner les objets contenus dans le dessin vectoriel, et de leur associer une action à réaliser.
		Trois types de profils peuvent être créés dans Visicut (menu Options>Profiles)
Line profile
Raster profile
Raster 3D profile


Line profile
Usage : découpe (cut) et gravure vectorielle (marquage – mark)

Options découpe :
résolution (dpi) : nombre de points par inch (25.4mm). Par exemple, à 100dpi, deux points consécutifs seront distants au minimum de 25.4/100=0.254mm. Cette résolution agit aussi sur le nombre de côté du polygone utilisé pour approximer un cercle ou une courbe.

épaisseur de trait représentée (si on veut découper un trait plus large, il fera plusieurs passages afin de couvrir l’épaisseur)
Optimization : du chemin parcouru par la tête laser (nearest conseillé).

Options marquage :
Identiques à ceci près que l’on décoche « is cut… , not just engraved »


Raster profile
Usage : gravure RASTER point par point (« aplat ») des images noir et blanc

Chaque face de chaque cube est gravé en raster Floyd-Steinberg.

Options RASTER :
résolution (dpi) : nombre de points par inch (25.4mm). Par exemple, à 100dpi, deux points consécutifs seront distants au minimum de 25.4/100=0.254mm. Cette résolution agit sur le nombre de points (blancs et noirs) qui formeront le nuage représentant la surface colorée. Trop faible : points isolés. Trop forte : les points noirs, tellement rapprochés, se brûlent les uns les autres.
Dithering Algorithm : Floyd-Steinberg (recommandé), HalfTone.
Grayscale Shift : curseur non gradué permettant de décaler les valeurs. Imaginons un carré gris à 50%, sa valeur de gris vaut donc 128. Si on lance un algorithme de dithering, on va créé un nuage de pixels dont un point sur 2 sera noir. Le curseur permet de moduler ceci en ajoutant une valeur au gris rencontré dans l’image. Curseur à gauche : on ajoute (-255) et curseur à droite +255. Ainsi, si on décale le curseur à droite d’un quart (+64), la valeur du gris à coder deviendra 128+64=192 : gris beaucoup plus clair, donc nuage plus clairsemé de points noirs. Si on décale le curseur à fond à droite, on obtient 128+255=383, plafonné à 255, soit blanc, et l’algorithme ne créera aucun point noir. Réglage assez sensible (+255 est possible, car alors le noir , initialement 0, sera transformé en 0+255 : blanc).


Raster 3D profile

Usage : gravure RASTER3D point par point (« aplat ») des images gris



Options RASTER 3D:
résolution (dpi) : nombre de points par inch (25.4mm). Par exemple, à 100dpi, deux points consécutifs seront distants au minimum de 25.4/100=0.254mm. Cette résolution agit sur le nombre de points gris qui formeront le nuage représentant la surface colorée. Trop faible : points isolés. Trop forte : les points, tellement rapprochés, peuvent se brûlent les uns les autres et donc rendre l’image trop foncée
Grayscale shift : là encore possibilité de moduler la noirceur (curseur -255 à 255).

Format de fichier .PLF
Le format .SVG ne contient que les objets vectoriels, et rien concernant les profils laser associés. Pour garder trace des associations objets-profils, il faut enregistrer sous dans Visicut. On crée ainsi un nom de fichier COURBURE.PLF.

Il s’agit d’un format compressé (on peut l’ouvrir et le décompresser avec 7-zip…), encapsulant 3 éléments :
Le fichier .SVG initial (sans correspondance de profils)
Un fichier transform.xml décrivant les transformations géométriques effectuées sous Visicut (placement, redimensionnement).
Un fichier mappings.xml décrivant la table des correspondances objets et profils laser tels qu’ils ont été définis dans l’onglet Mapping

En réouvrant ce .PLF avec Visicut à l’avenir, ces 3 fichiers permettront à Visicut de rouvrir le .SVG, le redimensionner et le replacer sur la table de travail, et d’associer aux objets les profils laser. En revanche, si on réouvre le .SVG (dans Inkscape>Extension>LaserCut PAth>Open in Visicut) il faut tout refaire…

Remarque : en revanche, aucune information concernant Vitesse et Puissance Laser n’ont été enregistrées. Les valeurs par défaut des profils laser utilisés seront reprises. Ce choix est délibéré, les auteurs considérant que le fichier .PLF devait être indépendant de tout matériel ; le choix puissance/laser dépendant de la machine et du matériau à découper, cela est cohérent. Il faudra donc redéfinir à chaque réouverture ces paramètres.


Définition des paramètres Vitesse/Puissance du laser

Onglet Laser Settings

Une fois le mapping effectué, l’onglet Laser Settings fait apparaître l’ensemble des profils laser utilisés et la liste des couleurs auxquelles chaque profil est associé (on a choisi un mapping par stroke color ici).
On a la main sur 3 paramètres :
Power : puissance du laser [ 0 – 100 ] %
Speed : vitesse de déplacement laser actif [0 – 100] % (100% correspond à 3000mm/min)
Focus : décalage vertical (en Z) de la lentille. En théorie, vous avez réglé la hauteur de la lentille au-dessus du matériau de façon à respecter la focale de la lentille [à la FABrique du Loch, lentille de focale 2.5’’ = 63.5mm. De cette façon, le laser est focalisé de façon très précise sur le matériau. Lorsque l’on veut graver des matériaux épais, il peut être judicieux de focaliser le faisceau non pas en surface mais dans l’épaisseur. Il peut être aussi utile de défocaliser sciemment le faisceau pour graver des traits plus larges (en éloignant la lentille de la surface du matériau de quelques milimètres)…

Remarque : en pratique, la machine ne modifie pas l’altitude de la lentille mais la hauteur du plateau (bed). Actuellement, un problème d’alignement des palliers empêche tout réglage de la hauteur du plateau à la FABrique : ne pas utiliser ce paramètre pour générer le GCODE. En revanche, initialement, on peut volontairement régler la tête laser à une altitude différente de la distance focale.







Remarque diamètre faisceau laser et résolution

Supposons travailler avec une lentille de focale f=2.5’’=63.5mm. Alors la largeur du rayon laser focalisé vaut 0.007’’ : deux points voisins ne se toucheront pas s’ils sont distants de 0.007’’, ce qui entraîne une résolution maximale de 1/0.007=142dpi… Au-delà on risque de surbrûler. Vouloir graver en RASTER 1000dpi semble totalement illusoire. En pratique, si on prend un rayon de 0.005’’, cela conduit à une résolution maximale de 1/0.005 = 200 dpi ce qui semble être une valeur plafond.

Source  http://www.engraversnetwork.com

Ces paramétrages ne sont pas enregistrables par Visicut (le format .PLF ne les contient pas).

Format de fichier .GCODE

Une fois le mapping effectué, et les paramètres laser choisis, on peut générer le fichier G-CODE correspondant au travail à effectuer. Ce fichier contiendra toutes les opérations élémentaires à effectuer par la machine (liste de tous les déplacements, des puissances/vitesses/focus laser successifs).

Menu File>Export laser code.







OCTOPRINT

Ouvrir un navigateur et entrer l’adresse IP : 102.168.1.41, découpe laser en marche. L’interface Octoprint s’ouvre alors et se connecte à la machine.

Cette interface permet de :
Uploader le fichier G-CODE dans la machine
Estimer le temps d’exécution
Lancer le job (on suppose que le matériau est en place, la lentille positionnée au zéro du fichier, le focus réglé en fonction de la focale de la lentille.
Contrôler le déroulement grâce à la vue caméra.



NUANCIER POUR LA DÉCOUPE/GRAVURE VECTORIELLE

En fonction du matériau, on peut choisir un couple (Puissance,Vitesse) du laser approprié. Le nuancier permet de simuler la découpe d’un disque de diamètre 10mm pour plusieurs choix de Puissance et de Vitesse :

  "https://www.lafabriqueduloch.org/projet/nuancier-decoupe-vitesse-puissance/"https://www.lafabriqueduloch.org/projet/nuancier-decoupe-vitesse-puissance/



CHOIX DE LA RÉSOLUTION POUR LA DÉCOUPE/GRAVURE VECTRIELLE DE COURBES
Le nuancier DPI représente la gravure des motifs suivants pour les résolutions 100, 150, 200, 333, 500, 1000 dpi. Plus les lignes sont droites, et moins il est besoin de recourir à des résolutions élevées.

  "https://www.lafabriqueduloch.org/projet/nuancier-decoupe-vitesse-dpi/"https://www.lafabriqueduloch.org/projet/nuancier-decoupe-vitesse-dpi/

NUANCIER RASTER FLOYD-STEINBERG

  "https://www.lafabriqueduloch.org/projet/nuancier-raster-floyd-steinberg/"https://www.lafabriqueduloch.org/projet/nuancier-raster-floyd-steinberg/
  "https://www.lafabriqueduloch.org/projet/nuancier-raster3d/"https://www.lafabriqueduloch.org/projet/nuancier-raster3d/
  "https://www.lafabriqueduloch.org/projet/nuancier-focale/"https://www.lafabriqueduloch.org/projet/nuancier-focale/


Dimensions :	320mm X 390mm
Vitesses :	 60%, 80% , 100%
Puissances :	10%, 20%, 30%, 40%

Pour chaque choix (Vitesse,Puissance) sont gravés :
un motif CUBE à 3 faces, colorées respectivement :
en GRIS 10% [RGB=(230,230,230)]
en GRIS 25% [RGB=(191,191,191)]
en GRIS 50% [RGB=(128,128,128)]
en 4 résolution : 100dpi, 200dpi, 333dpi et 500dpi

Visuel du motif :

Pour chaque couple (Puissance,Vitesse), on grave en RASTER selon 4 résolutions :


Simulation du nuancier :



Nuancier RASTER Floyd-Steinberg :
En abscisses Vitesse=[60,80,100] %
En ordonnées Puissance=[10,20,30,40] %

POUR ALLER PLUS LOIN

Inkscape :

Inkscape les effets de chemin "Croquis et Hachures" pour gravure laser
  "http://carrefour-numerique.cite-sciences.fr/fablab/wiki/doku.php?id=trucs_astuces:inkscape_les_effets_de_chemin_croquis_et_hachures_pour_gravure_laser"http://carrefour-numerique.cite-sciences.fr/fablab/wiki/doku.php?id=trucs_astuces:inkscape_les_effets_de_chemin_croquis_et_hachures_pour_gravure_laser
Inkscape Image to Vector
  "https://www.youtube.com/watch?v=XNEnQW_rOGw"https://www.youtube.com/watch?v=XNEnQW_rOGw
  "https://www.youtube.com/watch?v=7BFa0k6FJcc"https://www.youtube.com/watch?v=7BFa0k6FJcc



Générateur de boîte à encoches :
  "http://carrefour-numerique.cite-sciences.fr/fablab/wiki/doku.php?id=machines:decoupe_laser:trucs_astuces:generateur_boite_encoches"http://carrefour-numerique.cite-sciences.fr/fablab/wiki/doku.php?id=machines:decoupe_laser:trucs_astuces:generateur_boite_encoches

Générateur de packaging :   "http://www.templatemaker.nl/"http://www.templatemaker.nl/

Entretien de la machine
  "http://carrefour-numerique.cite-sciences.fr/fablab/wiki/doku.php?id=machines:decoupe_laser:0_utilisation:entretien"http://carrefour-numerique.cite-sciences.fr/fablab/wiki/doku.php?id=machines:decoupe_laser:0_utilisation:entretien

Procédure d’alignement des miroirs
  "http://justaddsharks.co.uk/support/laser-beam-alignment-guide" http://justaddsharks.co.uk/support/laser-beam-alignment-guide
  "http://www.rabbitlaserusa.com/Manuals/BeamAlignment.html" http://www.rabbitlaserusa.com/Manuals/BeamAlignment.html

Entretien LASER

  "https://www.youtube.com/watch?v=3mITnlN_6Dg"https://www.youtube.com/watch?v=3mITnlN_6Dg





L. Beguin 	La FABrique du Loch	 novembre 2017

Auteurs / contributeurs :
  L. Béguin – La Fabrique du Loch

Matériel : Découpeuse laser Robotseed RS-1610L + contrôleur Smoothieboard

Logiciels: Inkscape, Visicut, Octoprint
