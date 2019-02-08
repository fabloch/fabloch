# TUTO Broderie numérique avec Inkscape
## Motif
### Inkscape et Ink/stitch
#### préparer son motif
Nous allons partir d’un motif que vous avez fait vous même ou récupérer d’internet.

Tout d’abord, importez votre motif dans Inkscape

Vectorisez-le (**clic droit → vectoriser un objet matriciel**)

Assurez-vous d’en faire un chemin (**Ctrl+Maj+c OU chemin → objet en chemin**) afin que le logiciel soit capable de le convertir en  broderie et, si besoin, simplifiez-le (**Ctrl+l**) une ou deux fois afin d’éviter une broderie inutilement complexe (note : dans certains cas, un motif trop complexe engendrera tout simplement un refus de conversion de la part du plugin Inkstitch)

Une fois votre forme de base préparée, il est temps de faire les réglages de la broderie.
Pour ce faire, allez dans **Extension → Ink/Stitch → français** où vous trouverez les options suivantes
![image1](./assets/images/brodeusetuto1.jpg)
1. Broder… : exporte votre fichier de broderie
2. commandes : donne accès à différentes commandes de brodeuse comme couper le fil ou ignorer un élément
3. imprimer : préparer un aperçu pour faire notamment un bon de commande, avoir une estimation du temps de travail
4. lettering : permet de faire un lettrage basique (encore en développement)
5. installer des extensions pour inkscape : à permis l’installation de la palette brother
6. paramètres : permet de configurer la broderie pour obtenir le résultat souhaité
7. Satin Tools : permet de gérer les broderies de type satin à partir de lignes simple (encore en développement)

Ink/Stitch détecte automatiquement le type de travail recherché en fonction des éléments de votre forme (par exemple un fond est un remplissage par défaut) et les ordonne de la couche inférieure vers la couche supérieure.

Pour avoir les réglages qui vous conviennent, sélectionnez votre forme puis allez dans
Extension → ink/stitch → français → paramètres
Vous vous retrouverez alors face au menu suivant :
![image2](./assets/images/brodeusetuto2.jpg)

comme vous pouvez le voir, ce menu offre également un aperçu « en temps réel » vous permettant ainsi de faire des essais sur les différents paramètres proposés et d’avoir une idée approximative du résultat final.
#### le remplissage
**ATTENTION !
Cette section, ainsi que la suivante, part du principe que vous utilisez un tissu qui n’as pas de sens particulier et que votre forme reste assez simple.
Je recommande d’avoir un échantillon « test » de votre tissu vous permettant de vérifier vos réglages avant de vous lancer dans une broderie complète.**

Ink/stitch à détecter que vous vouliez faire un remplissage, et vous êtes face à une pile de réglage auxquels vous ne comprenez rien car vous ne vous y connaissez pas (encore) en broderie, pas de soucis : voici quelques conseils pour avoir un remplissage correct facilement.

Tout d’abord, allez dans l’onglet « sous-couche de remplissage automatique » et cochez la case « sous-couche ».
Maintenant changez la valeur « angle» pour qu’elle ai un décalage de 90° entre la sous-couche et le remplissage.
Enfin, changez l’espacement entre les lignes, en général une différence de 0,05 entre la sous-couche et le remplissage (espacement plus gros pour la sous-couche) donne un résultat plutôt correct.
#### le contour
Une méthode pour ne pas se prendre la tête au moment de faire un contour consiste à grossir le contour d’un objet (fenêtre fond et contour → Style de contour → épaisseur) puis de le convertir en chemin (chemin → contour en chemin) le contour deviendra donc un remplissage, il ne vous reste plus qu’à suivre les instruction en 1.1.b
#### exporter son motif
Maintenant que votre forme est prête, enregistrez votre fichier puis lancez l’exportation de celui-ci en tant que motif de broderie. Pour se faire, allez dans Extensions→ Ink/Stitch → Français →  Broder…

Cela vous ouvre un menu pour choisir le format (pour la brother, prenez .pes) ainsi que la destination du fichier de broderie.
Choisissez un support USB comme destination

Cliquez sur Appliquer, Ink/Stitch va alors lancer l’export du fichier de broderie sous un nom de type <nom_du_fichier>.pes.

Au cas où vous exporteriez plusieurs fois au même endroit un fichier de broderie à partir du même motif, Ink/Stitch sauvegarderais alors le nouveau fichier sous le nom <nom_du_fichier>.pes puis renommerait l’ancien fichier <nom_du_fichier>.pes.1 en allant de 1 à 5 avant d’écraser les versions les plus anciennes.

### Le lettrage
La meilleure solution concernant le lettrage pour l’instant est tout simplement de convertir un texte tapper avec Inkscape en chemin de broderie.

Pour se faire, tapez votre texte tel que vous le souhaitez à l’aide de l’outil écriture d’Inkscape.
Assurez-vous d’avoir un fond valide puis faites chemin → objet en chemin.
Maintenant, votre texte sera considérer comme un objet brodable classique.
## Machine
### Préparer la machine
#### Mise en place du fil
Commencez par mettre la machine sous tension à l’aide du bouton on/off situé sur sa droite.
Elle affichera alors une annonce pour prévenir du déplacement du support de broderie, appuyez juste sur « ok » sur l’écran tactile et la machine sera prête à l’emploi.
**VÉRIFIEZ LE NIVEAU DE LA CANNETTE !
Pour se faire, regardez dans la trappe située au milieu de la machine, vous y verrez une petite bobine, il s’agit de la cannette.
Si jamais cette dernière se vide pendant votre broderie, la machine arrêtera le travail en cours et vous vous verrez contraint de changer la bobine en cours de route.
Si jamais la canette est vide, ou trop peu remplie pour faire tout votre travail, référez-vous à la section 1.3 : que faire si la cannette est vide ?**
Assurez-vous que le pied-de-biche et l’aiguille soient relevés, si ce n’est pas le cas ,vous pouvez  y remédier à l’aide des boutons « position aiguille » et « Position pied-de-biche » (ou du levier à l’arrière de la machine).
#### préparation de la surface de broderie
#### Que faire si la cannette est vide ?
### importer son motif et démarrer la broderie
