# Drawbot

	•	Prendre une photo devant un fond blanc et de semi-profil pour voir ton nez !

	•	Ouvrir GIMP

  ouvrir photo jpg

	•	Ouvrir INKSCAPE
		redimensionner à la page
		supprimer ancien fichier
	  enregistrer sous en .svg simple

	•	Ouvrir internet TINKERCAD (compte)
	créer une conception
	importer fichier svg
	exporter en stl

	•	Ouvrir REPETIER
	placement d'objets
	charger fichier stl
	tailler de l'objet à la page (changer x) + z (drawbot Fred ) : 0,02
	(pour jouer avec la configuration du mode de crayon :
	configuration ou infill ou fil angle:0 ; 20

	•	Enlever CARTE SD



  Programmes utilisés :
  Gimp -> https://www.gimp.org/downloads/
  Inkscape -> https://inkscape.org/en/release/
  SpiralFromImage -> https://github.com/krummrey/SpiralFromImage
  https://code.google.com/archive/p/eggbotcode/downloads

  Extensions inkscape utilisées :

  Gcodetools (intégrée à inkscape) -> https://github.com/cnc-club/gcodetools
  Eggbot -> https://github.com/evil-mad/EggBot/releases/
  Centerline-trace -> https://github.com/fablabnbg/inkscape-centerline-trace/releases

  Sources :
  https://wiki.evilmadscientist.com/TSP_art

  Type de dessins :
  	•	Texte hershey
  	•	Texte depuis image ( Ex: Signature )
  	•	Dessin depuis image ( Ex: Croquis )
  	•	Voronoi
  	•	Delaunay
  	•	TSP ( Travelling Salesman Problem )
  	•	Spiral
  	•	CrossHatch
  	•	Halftone
  Chemin depuis image de Texte ou dessin (Images Matricielle)

  Pour dessiner du texte ou des dessins au drawbot, nous voulons une seul ligne, or, la vectorisation d’une image vectorielle nous donne des formes pleines. Pour remédier à cela, nous utilisons l’extension “Centerline Trace”.

  Installez l’extension :
  https://github.com/fablabnbg/inkscape-centerline-trace/releases

  puis :
  	1)	Importer image matricielle dans inkscape
  	2)	Sélectionner l’image puis “Extensions > Image > Centerline Trace”
  	3)	Jouer avec les paramètres puis “Appliquer”
  	4)	L’image vectoriel est placée par dessus l’image source

  ( Il est possible de lisser le texte via “Chemin > Simplifier” (Ctrl+L) )

  Ex de résultat :

  Texte Manuscrit Hersey

  “Hershey Text” est une extension inkscape très utile pour écrire du texte dans une police adaptée au Drawbot.

  	1)	Extensions > Rendu > Texte Hershey
  	2)	Entrer le texte voulu
  	3)	Sélectionner l’action : “Composer le texte”
  	4)	Choisir une police (l’action “Generate table of font sample” permet de visualiser toutes les polices)
  	5)	“Appliquer” (ou cocher “Aperçu en direct” avant pour prévisualiser le résultat)

  Polices disponibles :

  Nuage de points (pour TSP/Voronoi/Delaunay)
  	1)	Importer une image dans Gimp
  	2)	Image > Mode > Niveaux de gris
  	3)	Couleur > Niveau : éclaircir l’image
  	4)	Image > mode > Couleurs indexées
  	a)	Utiliser la palette noir & blanc (1-bit)
  	b)	Tramage des couleur : Floyd-Steinberg (Normal)
  	c)	SVG vers GCODE

  	1)	Extension > Gcodetools > Points d’orientation :
  	2)	“Appliquer”
  	3)	Extension > Gcodetools > Bibliothèque d’outils
  	4)	“Appliquer”
  	5)	Sélectionner le chemin
  	6)	Extension > Gcodetools > Chemin vers Gcode…
