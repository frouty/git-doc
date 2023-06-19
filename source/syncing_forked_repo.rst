Comment mettre à jour un repo forked
####################################

Dans le web
***********
On va sur la page principale du repository et on cherche *sync fork*

Mais on ne sync que branche par branch. 

   - 1 clone de la fork en local ::
      
      git clone blablal
      
   - 2 add en remote l'url du repo forké ::
   
      git remote -v
      git remote add upstream urlduprojetforké.
      git remote -v .  
      
    - 3 fetch ::
         git fetch upstream
         ou git pull upstream et il faut faire branche par branche. C'est pénible pour odoo car il y en a bcp.
         