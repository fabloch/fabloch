# Tuto Hurlomaton 

 1) Vérifier les connexions des composants, la fixation de la caméra et les branchements électriques.

2) une fois toutes ces vérifications effectuées, on branche l’alimentation générale pour lancer la machine. Puis on allume l’imprimante. 
3) Ouvrir le navigateur Web Chromium (raccourci sur le bureau)

4) ouvrir le signet imprimante et vérifier si l’état est noté comme « inoccupé » Si c’est le cas, on peut fermer la fenêtre . 

5) pour que la cabine soit opérationnelle, il faut lancer 4 scripts contenus dans le dossier « hurlomaton » présent sur le bureau.

Pour lancer les scripts, on va procéder ainsi :

On commence par ouvrir le terminal en cliquant avec le bouton droit de la souris sur l’icône du dossier « hurlomaton » puis en sélectionnant « Ouvrir dans le terminal ».

Une première fenêtre s’ouvre. Dans la barre d’outils, on va cliquer sur « Fichier » puis « New Tab » pour ouvrir une seconde fenêtre et on recommence jusqu’à avoir 4 fenêtres ouvertes sur son bureau.

Dans chacune de ces fenêtres, on voit la même ligne suivante :
(hurlo) pi@raspberrypi:~/Desktop/hurlomaton $

Pour lancer les scripts, on va ajouter une ligne de commande dans chaque fenêtre :

Pour lancer le script 1, on va taper ceci :
py script_1_crop_watch.py

On valide la commande avec la touche Entrée

Pour le script 2 :
script_2_upload_watch.py

Pour le 3 :
script_3_print_watch.py

Pour le 4 :
script_4_hurlomaton.py

6) Le Hurlomaton est normalement prêt à fonctionner.  7) Pour quitter le Hurlomaton , taper sur F.
Pour arrêter complètement la machine, il faut simplement arrêter l’ordinateur.  
