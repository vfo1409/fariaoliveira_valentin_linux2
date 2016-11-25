TP2
=========

## Configuration de la passerelle

### Configuration matérielle

La VM Gateway dispose de trois cartes réseau:

* une carte avec accès par pont qui sera relié au réseau extérieur

* une carte en mode réseau interne qui sera sur relié au réseau des machines clientes

* une carte sur le même mode réseau interne qui sera relié au réseau des serveurs

### Openssh

La VM est connecté au réseau avec l'adresse 192.168.99.186 et dispose de deux utilisateurs: root et val. Sur l'hôte, la connexion à la VM en tant que val ce fait par la commande suivante:
    ssh 192.168.99.186 -l val

Une fois la connexion effectué, la VM demande le mot de passe utilisateur et permet l'utilisation de ligne de commande.
Afin de prouver que la connexion est bien effective, on crée via ssh un fichier test, qui se voit sur la VM.

![Test de la connexion ssh](https://raw.githubusercontent.com/vfo1409/virtualisation/master/Images/sshtest.png "Test de la connexion ssh")

Lors d'une tentative de connexion en tant que root, l'accès est refusé malgré l'entrée du bon mot de passe par mesure de sécurité. Il est toutefois possible d'utiliser la commande `su` en tant qu'utilisateur.
