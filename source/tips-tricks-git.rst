Connaitre la différence entre un meme fichier de deux branches  différentes
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

# Comment récuperer une nouvelle branch remote inconnue localement.
git fetch --all
git checkout 

Voir tous les fichiers tracked par le git repo
##############################################

:: 

   git ls-tree --full-tree -r --name-only HEAD