TP1
========

## Sudo

Il faut toujours éditer le fichier sudoers par la commande `visudo` et non pas manuellement car, selon le manuel de sudoers, visudo và verouillé le fichier et effectuer une vérification grammatical pour être sur que le plugin sudoers fonctionne correctement.

Ne faisant partie que de mon propre groupe, je n'ai pas les droits pour utiliser la commande visudo.

![Message d'erreur de visudo](https://raw.githubusercontent.com/vfo1409/fariaoliveira_valentin_linux2/master/img/sudo.png "Message d'erreur de visudo")

Après modification du fichier sudoers via `visudo`, l'utilisation de `sudo` avec des commandes réservées au superutilisateur par un utilisateur lambda (ici val) est possible.

![Fichier sudoers modifié](https://raw.githubusercontent.com/vfo1409/fariaoliveira_valentin_linux2/master/img/sudoers.png "Fichier sudoers modifié")
