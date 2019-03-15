# bash

Accéder depuis un mac à un répertoire sur un serveur
https://superuser.com/questions/164624/accessing-shared-directory-path-in-mac-os-x-terminal
```
$ cd /Volumes/<Serveur>
```

Lister tous les répertoires et les fichiers d'un volume
https://stackoverflow.com/questions/105212/linux-recursively-list-all-files-in-a-directory-including-files-in-symlink-direc


Compter le nombre de fichiers d'un certain type dans une arborescence de répertoires.
```
$ find . -name "*.YOURFILETYPE" | wc -l
```





https://stackoverflow.com/questions/10929453/read-a-file-line-by-line-assigning-the-value-to-a-variable
https://stackoverflow.com/questions/24411185/splitting-string-separated-by-comma-into-array-values-in-shell-script
https://stackoverflow.com/questions/3685970/check-if-a-bash-array-contains-a-value
https://unix.stackexchange.com/questions/110645/select-lines-from-text-file-which-have-ids-listed-in-another-file

```


# ------------------------------------------------------------------------------
#
# Nice treatment
#
# OLDIFS=$IFS
# IFS=";"
# while read user job uid location
#  do
#
#     echo -e "$user \
#     ======================\n\
#     Role :\t $job\n\
#     ID :\t $uid\n\
#     SITE :\t $location\n"
# done < $1
#  IFS=$OLDIFS


#while IFS='' read -r line || [[ -n "$line" ]]; do
#    # echo "Text read from file: $line"
#    variable=$1
#
#    for i in $(echo $variable | sed "s/;/ /g")
#    do
#        # call your procedure/other scripts here below
#
#        echo "$i"
#    done
#done < "$1"
```
