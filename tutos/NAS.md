# Le NAS de la fabrique

Voir présentation sur le site :
https://www.openmediavault.org/about.html

## Paramétrages divers

Sur le NAS
les deux disques de 250 Go sont montés en RAID1 (miroir)
permet de conserver les données en cas de panne d'un des deux disques mais ne constitue pas une sauvegarde
envisager back-up journalier et sauvegarde mobile

Un dossier partagé en accès public (sans mot de passe) « fabrique »
établir une structure : dossiers personnels pour fichiers temporaires et dossiers par machine, activité,  type de fichier ???

ex : Projets, machines, logiciels, photos, informatique, logiciels, hardware ????


Dossiers avec mots de passe possible : buro
un utilisateur et mot de passe partagé
un accès pour chaque personne


allumage du nas : s’assurer qu’aucun périphérique USB bootable n’est branché

extinction du nas : appui long sur la touche d’extinction (à programmer dans le backoffice)

Sur les ordinateurs :

Parcourir réseau dans la colonne de gauche du navigateur de fichiers et se connecter sur  NAS-OMV

Accès au nas par les applications (pour enregistrer) : ajout d'une fonction dans le terminal
cf : https://doc.ubuntu-fr.org/tutoriel/acceder_a_votre_nas_depuis_toutes_les_applications

montage automatique sur le bureau : modification de fstab
 la ligne 17 dans /etc/fstab est erronée
mount : seul le superutilisateur peut monter //192.168.1.49/share sur /media/fabrique

https://doc.ubuntu-fr.org/mount_fstab

https://www.debian-fr.org/t/mount-et-fstab-pour-les-nuls/22623

cf : https://forum.ubuntu-fr.org/viewtopic.php?id=748201
et




sudo mount //192.168.1.49/share /media/fabrique
[sudo] password for ubu:
mount : mauvais type de système de fichiers, option erronée, superbloc erroné
        sur //192.168.1.49/share, page de code ou programme auxiliaire manquant, ou autre erreur
       (pour plusieurs système de fichiers (NFS ou CIFS par exemple), un
        programme /sbin/mount.<type> auxiliaire pourrait être nécessaire)
       Dans quelques cas certaines informations sont utiles dans le journal
        système — essayez « dmesg | tail » ou quelque chose du genre


montage dossier fabrique
sudo mount.cifs //192.168.1.49/fabrique /media/fabrique -o guest

le fstab actuel :

# /etc/fstab: static file system information.
#
# Use 'blkid' to print the universally unique identifier for a
# device; this may be used with UUID= as a more robust way to name devices
# that works even if disks are added and removed. See fstab(5).
#
# <file system> <mount point>   <type>  <options>       <dump>  <pass>
# / was on /dev/sda5 during installation
UUID=815e16bc-40d6-4f29-9b17-4bf217eea604 /               ext4    errors=remount-ro 0       1
# swap was on /dev/sda6 during installation
UUID=6a8482c8-f706-480e-b82a-58c8213f8440 none            swap    sw              0       0
# Monter NAS
//192.168.1.49/fabrique    /media/fabrique cifs    guest,iocharset=utf8,gid=100,uid=1000,_netdev   0       0

#swap
/dev/sda1       swap    swap    defaults        0       0
#UUID=8bc71292-90a9-40aa-bf19-a5d4a98b3856
