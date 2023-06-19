Customizing git
###############

Git configuration
*****************

Git va lire les fichiers de config dans :

- 1 /etc/gitconfig. 
- git config --system va lire/ecrire dans ce fichier: /etc/gitconfig.
- 2 ~/.config/git/config ou ~/.gitconfig. 
   - git config --global va lire/ecrire dans ce fichier.
- 3 dans le fichier de configuration du directory dans le quel on est ./.git/config
   - git config --local pour lire écrire dans ce fichier ./.git/config.

Comment voir tous les settings
******************************
::

   git config --list --show-origin