# Owncloud

## Description

Owncloud est un service de synchronisation avec une cloud. Le fonctionnement ressemble à cella de OneDrive ou de Dropbox.

## Installation

* Telechargement depuis https://software.opensuse.org/download/package?project=isv:ownCloud:desktop&package=owncloud-client

  ```Bash
  # Exemple Ubuntu
  echo 'deb http://download.opensuse.org/repositories/isv:/ownCloud:/desktop/Ubuntu_20.04/ /' | sudo tee /etc/apt/sources.list.d/isv:ownCloud:desktop.list
  curl -fsSL https://download.opensuse.org/repositories/isv:ownCloud:desktop/Ubuntu_20.04/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/isv_ownCloud_desktop.gpg > /dev/null
  sudo apt update
  sudo apt install owncloud-client
  ```

* Lancer owncloud depuis un terminal avec la commande: `owncloud`
* Mettre l'adresse de serveur `https://drive.switch.ch`
* Connecter vous avez votre compte (si le compte [prenom].[nom]@heig-vd.ch ne fonctionne pas, essayer de créer un compte avec cette adresse)
* Préciser `Local Folder` pour dire dans quelle dossier les fichiers seront synchronisé.
* OwnCloud est configuré
* Si owncloud ne démarre pas au démarage du système, faites de recherches pour mettre la commande `owncloud &` dans un script de démarrage propre à votre distribution (Startup script)

