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


