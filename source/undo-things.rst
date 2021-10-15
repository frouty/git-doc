===============
 Undo with git
===============

Workflow git
------------

1. You create or edit a file. Il est unstaged. Il n'est pas encore tracké par git

2. You add the file to the repository : **git add**. Qui place le fichier dans l'état staged.

3. You commit sur le repository local: **git commit**

4. You push the file to a remote repository: **git push**


Undo local changes
------------------

Undo unstaged local changes : before git add
********************************************

1. Annuler les changements : **git checkout <file>**. On checkout la version du fichier.
2. Sauvegarder  les changements pour pouvoir les utiliser plus tard: **git stash**
3. Pour annuler tous les changements de tous les fichiers, de facon permanente: **git reset --hard**

Undo staged local files
***********************
