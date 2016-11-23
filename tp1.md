TP1
========

## Sudo

Il faut toujours éditer le fichier sudoers par la commande `visudo` et non pas manuellement car, selon le manuel de sudoers, visudo và verouillé le fichier et effectuer une vérification grammatical pour être sur que le plugin sudoers fonctionne correctement.

Ne faisant partie que de mon propre groupe, je n'ai pas les droits pour utiliser la commande visudo.

![Message d'erreur de visudo](https://raw.githubusercontent.com/vfo1409/fariaoliveira_valentin_linux2/master/img/sudo.png "Message d'erreur de visudo")

Après modification du fichier sudoers via `visudo`, l'utilisation de `sudo` avec des commandes réservées au superutilisateur par un utilisateur lambda (ici val) est possible.

![Fichier sudoers modifié](https://raw.githubusercontent.com/vfo1409/fariaoliveira_valentin_linux2/master/img/sudoers.png "Fichier sudoers modifié")


## Snapshot

Après avoir effectué un instantanée de la VM "debian_base" et lancé `rm -rf / --no-preserve-root` en tant que root, on remarque tout de même que certaint fichier de base, tel que etc, ne sont pas supprimé par manque de droit.

Néanmoins, le système est clairement instable et la majorité des programme comme ls inexistant.
Après un redémarrage forcé, le système de lancement ne trouvant pas le fichier "/boot/grub/i386-pc/normal.mod", qui est un module de grub contenant la commande `normal` permettant de lancer GRUB, entre alors en mode de secour.

![Mode de secour de GRUB](https://raw.githubusercontent.com/vfo1409/fariaoliveira_valentin_linux2/master/img/grubrescue.png "Mode de secour de GRUB")

Après avoir restauré l'instantané qui avait été fait avant le lancement de la commande `rm`, toutes les données se retrouve à nouveau sur le disque virtuelle et la VM démarre normalement.

## Configuration réseau


