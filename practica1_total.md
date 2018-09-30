## Comandos b醩icos I

Iniciar repositorio en un directorio:

`git init`

Agregar cambios al area de staging:

`git add`

Validar cambios en el repositorio:

`git commit -m " Mensaje "`

Hacer los dos pasos anteriores en uno:

`git commit -am " Mensaje "`

Historial de commits:

`git log`

## Comandos b醩icos II

Ayuda del listado anterior:

`git help log`

Listar los 5 commits m醩 recientes:

`git log -n 5`

Listar los commits desde una fecha:

`git log -- since =2018 -09 -18`

Listar los commits por autor:

`git log -- author =" Antonio "`

Ver cambios en el directorio:

`git status`

## Comandos b醩icos III

Ver diferencia entre ficheros en el directorio y el repositorio de git:

`git diff`

Ver diferencia entre ficheros en el staging y el repositorio:

`git diff -- staged`

Eliminar archivos:

~~~
git rm archivo
git commit -m " Mensaje "
~~~

Mover o renombrar archivos:

~~~
git mv antiguo nuevo

git commit -m " Mensaje "
~~~

## Comandos b醩icos IV

Deshacer cambios con git:

`git checkout -- nombre_fichero`

Retirar archivos del staging:

`git reset HEAD nombre_fichero`

Complementar 磚ltimo commit:

`git commit -- amend -m " Mensaje "`

Recuperar version de un fichero de commit antiguo:

`git checkout < id_commit > -- nombre_archivo`

Revertir un commit:

`git revert < id_commit >`

## Comandos b醩icos V

Deshacer multiples cambios en el repositorio:

~~~
git reset -- soft < id_commit >
git reset -- mixed < id_commit >
git reset -- hard < id_commit >
~~~

Listar archivos que git no controla:

`git clean -n`

Eliminar archivos que git no controla:

`git clean -f`

Ignorar archivos en el repositorio: .gitignore## COMANDOS BASICOS VI

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





## Comandos GitHub I

A帽adir repositorio remoto:

`git remote add origin url`

Ver repositorios remotos:

`git remote -v`

Eliminar repositorio remoto:

`git remote rm origin`

A帽adir cambios del repositorio local al remoto:

`git push -u origin master`

A帽adir cambios del repositorio remoto al local:

`git pull`





## Comandos GitHub II

Ver *branches* remotos:

`git branch -r`

Ver todos los *branches*:

`git branch -a`

Clonar un repositorio remoto:

`git clone url`





## Dar seguimiento a *branches* remotos

* LOCAL --> REMOTO
 1. Cambios en el repositorio local.
 2. Commit de los cambios.
 3. A帽adir cambios a repositorio remoto.

 `git push`

* REMOTO --> LOCAL
 * Sincronizaci贸n y uni贸n:

 ~~~
 git fetch origin
 git merge origin/master
 ~~~

 * En un solo paso:

 `git pull`





## Operaciones con *branches* remoto

* Creaci贸n:
 1. Crear branch local.
 2. Hacer cambios en dicho branch.
 3. Hacer commit.
 4. Copiar el branch al repositorio remoto:

 `git push -u origin branch_remoto`

* Copia:

`git checkout -b local remoto`

* Eliminaci贸n:

`git push origin --delete branch_remoto`
