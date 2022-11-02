Importer un projet existant
###########################

Importer dans le cloud un projet existant localement

aller à la racine du projet ::

   cd /path/racine/projet

initialiser le git ::

   git init
   git add --all
   git commit -m "initial commit"
   
log into bitbucket , create a new repository

trouver l'url du repository  (https://username@your.bitbucket.domain:7999 /yourproject/repo.git)

configurer le remote sur le projet local et pousser le projet dans le cloud ::

   git remote add origin https://username@your.bitbucket.domain:7999 /yourproject/repo.git url touvée plus haut
   git push -u origin master
   
Pas encore testé. 