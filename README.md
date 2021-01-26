# git-doc
# git workflow
[ici](https://www.synbioz.com/blog/tech/git-adopter-un-modele-de-versionnement-efficace)  
branche master code de production  
création d'un branche dev  
dev peut etre utilisée pour faire des tests, une pre-install  
Elle ne doit etre utilisée que pour les petites modifications.  
Creations de branches spécialisées pour des dévellopement de fonctionnalité  
`git checkout -b feature/foo dev` 
Une fois fini il faut merger dans dev:  
```
git checkout dev
git merge --no--ff feature/foo
git branch -d feature/foo
git push origin dev

``` 