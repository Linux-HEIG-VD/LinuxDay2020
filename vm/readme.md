## But

Travailler sur les machines virtuelle de l'école sans utiliser le bureau de la vm.

Explication:

* Lancer la machine virtuelle en mode **Headless**
* Accèss en SSH
* 

## Parametrage de la machine virtuelle

#### Adresse IP locale

Pour accèder à la machine toujours par la même adresse IP on doit connecter la machine à un réseau virtuel qui est partagé entre notre machine physique et toutes les machines virtuelles.



Avec cette manip, l'adresse IP sur la vm est en DHCP. Elle pourait changer à tout moment. Mais le serveur DHCP de virtualbox ne change normalement pas les adresse de ses clients.

##### Créeation du réseau Host-Only

Dans Virtualbox: File -> Host network manager -> create.

pas besoin de configurer le réseau plus que ça.

##### Connecter la VM au réseau locale

Dans Virtualbox: Séléctionner la machine virtulle -> Settings -> Network -> Adapter 2 -> Enable + Attached to : Host only Adapter

<img src="../img/vm_connect_to_net.png" style="zoom:80%;" />

##### Trouver l'adresse IP

* Demarrer la machine virtuelle.
* Ouvrez un terminal
* tapez la commande `ip a` ou  `ifconfig`  
  * Gardez en mémoire l'adresse IP du réseau locale (normalement du style 192.168.56.xxx)

## Sur la machine physique

