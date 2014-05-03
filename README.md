Plantilla para repositorios de git
=============

Un ejemplo de plantilla para repositorio de git. Tiene algún fichero traducido al español y un ejemplo de *hook* ligeramente modificado.

Instrucciones
----

Para sustituir a la plantilla por defecto de `git`

```
	sudo mv /usr/share/git-core/templates/ /usr/share/git-core/templates-orig # Quita de enmedio las plantillas originales
    sudo cd /usr/share/git-core && git clone git@github.com:JJ/repo-plantilla.git && mv repo-plantilla templates
```

Cada vez que hagas `git clone` o `git init` se usará esta plantilla para crear la estructura del repositorio bajo `.git` en vez de la que hay por defecto.

Por otro lado, también la puedes clonar en el directorio que quieras

```
	cd ~
	git clone git@github.com:JJ/repo-plantilla.git
	mv repo-plantilla .git-template
```

Si quieres quitar todos los ficheros que no sean estrictamente de la plantilla puedes borrarlos a mano antes de empezar a clonarlos, o bien usar la rama que ya los ha eliminado:

```
	cd ~
	git clone git@github.com:JJ/repo-plantilla.git --branch instalar
	mv repo-plantilla .git-template
```
	
Y luego usarlo con 

```
	git init --template=/home/miusuario/.git-template
``` 

Es importante que se ponga el camino completo a `.git-template` sin usar la abreviatura `~` del shell. 

Esta orden copiará todos los ficheros en el subdirectorio indicado al subdirectorio `.git`. Es posible que quieras borrar este fichero `README`, y activar el *hook* de ejemplo haciendo

```
	mv .git/hooks/prepare-commit-msg.ejemplo .git/hooks/prepare-commit-msg
```

que añade una firma (editable) a todos los mensajes de *commit*. 

	
	


