************
Git workflow
************
Workflow
========
`ici <https://www.synbioz.com/blog/tech/git-adopter-un-modele-de-versionnement-efficace>`_  

* branche **master** pour le code de production.
* création d'une branche **dev**  
* dev peut être utilisée pour faire des tests de production, une pre-install  

Elle ne doit etre utilisée que pour les petites modifications.  
Créations de branches spécialisées pour des dévelopement de fonctionnalités  

::

	git checkout -b feature/foo dev   

Une fois fini il faut merger dans dev:  
::

	git checkout dev
	git merge --no--ff feature/foo
	git branch -d feature/foo
	git push origin dev


Une fois que **dev** est dans un état satisfaisant pour passer en production il faut merger **dev** dans master.
On crée d'abord une branche de support à la release. Elle servira à faire des modifications mineures.  
::

	git checkout -b release/v1.2 dev 

On fait les modifications mineures puis:
::

	git checkout master 
	git merge --no-ff release/v1.2
	git tag -a v1.2

 
On récupère ces informations de release dans dev.  
::

	git checkout dev
	git merge --no-ff release/v1.2
	git branch -d release/v1.2
	
Dépanner les bugs en production
===============================
On ne passe pas par dev. On fait un hotfix qui est un patch intégré directement dans la branche de production et ensuite appliquée à la branche dev. 
::

	git checkout -b hotfix/v1.2.1 master
	git commit -a -m 'Bumped version number to 1.2.1'


On corrige le bug et on l'intégre en production
::

	git commit -m 'Corrige le gros bug'
	git checkout master
	git merge --no-ff hotfix/v1.2.1
	git tag -a v1.2.1


Mais également dans dev pour ne pas perdre le fix.
::

	git checkout dev
	git merge --no-ff hotfix/v1.2.1

Le fix est intégré dans **master** et **dev** et on peut le supprimer  
::

	git branch -d hotfix/v1.2.1