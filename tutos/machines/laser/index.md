---
title: Découpeuse laser de la Fabrique du Loch
---

# Découpeuse Laser de la Fabrique du Loch

Notre découpeuse laser est une **Robotseed RS-1610L** avec un **contrôleur Smoothieboard**.

Cette découpeuse permet de **découper** ou de **graver** différentes matières, notamment le MDF, très utilisé à la Fabrique!

  - Découpe vectorielle (cutting)
  - Gravure vectorielle (marking)
  - Gravure RASTER (aplat - engraving)
  - Gravure Raster 3D (3D engraving)

[Pour en savoir plus sur les différent usages](usages)

## Comment découper?

[Le mode d'emploi complet](utilisation)

A la FABrique, les étapes de la découpe laser sont les suivantes:

### Inkscape

- Etape 1: dessin vectoriel (fichier au format .SVG)

### Visicut

- Etape 2: association des dessins aux modes de découpe/marquage/gravure (fichier au format .PLF)
3. définition des paramètres laser (DPI, Vitesse, Puissance)
4. génération du G-CODE (fichier au format .GCODE)

### Octoprint

5. estimation du temps d’exécution, envoi du G-CODE vers la découpe Laser,  suivi du travail (caméra)

## Caractéristiques techniques

|   |   |
|---|---|
|  Type 	              | RobotSeed RS-1610L Laser Cutter   	|   
|  Laser 	              | 90W long-life RECI laser tube (CO2)  	|   	
|  Contrôleur 	        | Smoothieboard (open-source)  	|  
|  Zone de travail 	    | 1600 x 1000 mm  	|   
|  Résolution maximale 	| 0.025 mm (1000dpi)  	|  
|  Répétabilité 	      | 0.01 mm  	|
|  Langage 	            | G-CODE supporté par Smoothieboard  	|
|  Software 	          | Open interface with many options: Laserweb, Visicut, Octoprint, Cambam, Fusion 360, Inkscape, Illustrator  	|
|---|---|

- [Nuancier pour la découpe / gravure](nuancier)
- [Choix de la résolution pour la découpe / gravure vectorielle de courbes](resolution)

## Auteurs / contributeurs :
L. Béguin – La Fabrique du Loch
