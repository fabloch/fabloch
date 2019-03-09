# Problème d'échelle entre les .SVG Illustrator et Inkscape

Les fichiers .SVG sont sauvegardés avec des unités en pixels, cependant inkscape et illustrator utilisent des facteurs de conversion px/mm différents :

|--------------|----------------------------------|
| Illustrator  | 72dpi : 72 px = 1 inch = 25.4 mm |
| Inkscape 	   | 90dpi : 90 px = 1 inch = 25.4 mm |
|--------------|----------------------------------|

## Exemple

Supposons avoir créé un carré de côté 25.4mm dans Illustrator.

Lorsque vous enregistrez le fichier .SVG avec Illustrator, les dimensions sont converties en pixels avec le ratio 72dpi : on a donc un carré de côté 72 pixels.

En l’ouvrant dans inkscape (export .svg), il ouvre un fichier contenant un carré de 72 pixels, en utilisant un ratio de 90dpi pour retrouver les dimensions de l’objet. On obtient donc un carré de côté 72px/90dpi = 0.8 inch = 20.32mm.

Il est donc nécessaire dans Inkscape de redimensionner les objets créés avec Illustrator d’un facteur de 90/72 = 125% afin de conserver les dimensions originales (en mm).

## Comment corriger ce problème?

Pour redimensionner les SVG Illustrator d’un facteur 125% dans Inkscape:

1. Ouvrir le .SVG créé par Illustrator dans Inkscape
2. Tout sélectionner (Ctrl+A), grouper (Ctrl+G).
3. Dans le menu objet, transformer (Ctrl+Maj+M)
4. Dans la nouvelle fenêtre, onglet mise a l’échelle : 125% (largeur et hauteur)
5. Vérifier que les dimensions sont maintenant correctes.
