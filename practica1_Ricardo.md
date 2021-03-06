## COMANDOS BASICOS VI

*Listar el contenido del repositorio de git:*

~~~
git ls-tree master 
git ls-tree master^^^
git ls-tree master~3
~~~

*Log en una linea:*

`git log --oneline`

*Log con los tres ultimos commits en una linea:*

`git log --oneline -3`

## COMANDOS BASICOS VII

*Examinar el contenido de un commit:*

`git show <id>`

*comparar un commit con el actual:*

`git diff <id> nombre_archivo`

*comparar dos commits:*

`git diff id..id nombre_archivo`

## RAMAS O BRANCHES

**Es la forma para separar la linea actual de desarrollo con respecto a la principal. Normalmente representan versiones de software que posteriormente son integradas a la linea principal.**

## COMANDOS RAMAS I

*ver listado de ramas:*

`git branch`

*crear una rama:*

`git branch nombre_rama`

*cambiarnos un una rama:*

`git checkout nombre_rama`

*crear una rama y moverse en un paso:*

`git checkout -b nombre_rama`

*comparar ramas:*

`git diff nombre_rama..nombre_rama`

## COMANDOS RAMAS II

*ver ramas identicas a la actual:*

`git branch --merged`

*renombrar ramas:*

`git branch -m nombre_antiguo nombre_nuevo`

*eliminar ramas:*

~~~
git branch -d nombre_rama
git branch -D nombre_rama
~~~

*integrar ramas a la actual:*

`git merge nombre_rama`

*resolver conflictos:*

`git merge --abort`


## COMANDOS RAMAS III

*almacenar cambios temporales:*

`git stash save "Mensaje"`

*listar cambios:*

`git stash list`

*ver contenido de un cambio temporal:*

`git stash show -p nombre_stash`

*eliminar un cambio temporar:*

`git stash drop nombre_stash`

*aplicar cambio del stash:*

~~~
git stash apply nombre_stash
git stash pop nombre_stash
~~~





