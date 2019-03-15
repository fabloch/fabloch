# Tuto Hurlomaton

## Mise en marche

## Démarrage
 1. Vérifier les connexions des composants, la fixation de la caméra et les branchements électriques.
2. On branche l’alimentation générale pour lancer la machine.
3. Puis on allume l’imprimante. 

## Sur l'ordi

4. Ouvrir le navigateur Web Chromium (raccourci sur le bureau)
5. Ouvrir le signet imprimante et vérifier si l’état est noté comme « inoccupé »; Si c’est le cas, on peut fermer la fenêtre.
6. Pour que la cabine soit opérationnelle, il faut lancer 4 scripts contenus dans le dossier « hurlomaton » présent sur le bureau.

Pour lancer les scripts, on va procéder ainsi :

On commence par ouvrir le terminal en cliquant avec le bouton droit de la souris sur l’icône du dossier « hurlomaton » puis en sélectionnant « Ouvrir dans le terminal ».

Une première fenêtre s’ouvre.

Dans la barre d’outils, on va cliquer sur « Fichier » puis « New Tab » pour ouvrir une seconde fenêtre et on recommence jusqu’à avoir **4 fenêtres Terminal ouvertes sur son bureau**.

Dans chacune de ces fenêtres, on voit la même ligne suivante :
```
(hurlo) pi@raspberrypi:~/Desktop/hurlomaton $
```

Pour lancer le script 1, on va taper ceci dans une des fenêtres:
```
$ py script_1_crop_watch.py
```
On valide la commande avec la touche Entrée

Puis successivement on exécute les commandes suivantes dans les 3 autres fenêtres:

```
$ py script_2_upload_watch.py
```

```
$ py script_3_print_watch.py
```

```
$ py script_4_hurlomaton.py
```

Le Hurlomaton est normalement prêt à fonctionner!

# Arrêt
- Pour quitter le Hurlomaton , taper sur F.

- Pour arrêter complètement la machine, il faut simplement arrêter l’ordinateur.  
