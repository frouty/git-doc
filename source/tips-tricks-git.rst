Connaitre la différence entre un même fichier de deux branches  différentes
###########################################################################

::
   git difftool -t meld master:oph/oph/rt5100.py fixrt5100:oph/oph/rt5100.py
   
Connaitre la différence entre deux branches
###########################################
::

   git difftool -t meld master..fixrt5100`  

Commande qui va te proposer d'ouvrir meld pour chaque fichier à comparer. Faire quit meld pour passer au fichier suivant. 

Gestion des branches
####################

Connaitre le dernier commit de toutes les branches
**************************************************
:: 
   
   git branch -v
   
Voir les branches déjà mergées
******************************
::
   
   git branch --merged  
   
Et on peut les supprimer avec::
   
   git branch -d nomdelabranche  

Comment récuperer une nouvelle branch remote inconnue localement.
*****************************************************************
::
   
   git fetch --all
   git checkout 

Voir tous les fichiers tracked par le git repo
##############################################

:: 

   git ls-tree --full-tree -r --name-only HEAD
   
Comment faire qu'avec git init main soit la branche principale et pas master
############################################################################
   
:: 

   cd ~ 
   git  config --global init.defaultBranch main

Ca marche pas. ma version n'est pas la bonne. 

::
   mkdir -p ~/.config/cp -r /usr/share/git-core/templates/ ~/.config/git/
   git config --global init.templateDir '~/.config/git/templates'
   echo 'ref: refs/heads/main' > ~/.config/git/templates/HEAD
   
   