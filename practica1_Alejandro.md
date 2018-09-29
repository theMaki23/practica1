# Comandos b�sicos I

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

#Comandos b�sicos II

Ayuda del listado anterior:

`git help log`

Listar los 5 commits m�s recientes:

`git log -n 5`

Listar los commits desde una fecha:

`git log -- since =2018 -09 -18`

Listar los commits por autor:

`git log -- author =" Antonio "`

Ver cambios en el directorio:

`git status`

#Comandos b�sicos III

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

