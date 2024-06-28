## Comandos de GIt
* git init: Inicializar el programa de control de versiones
* ls -al: Ver los archivos del directorios actual
* code: Abre code en el directorio actual
* git add .: incluye todos los archivos en el dir a la version. Sube al Staging: MEmoria RAM. Estado temporal
* git add <letra> tab : autocompletado
* git rm <biografy.txt> : elimina el archivo <x> del commit.
* git commit -m "mensaje": Deja los archivos incluidos en un limbo con mensaje de version. Sube al repositorio master
* git config --list-show-origin: Me muestra elementos de configuracion necesaria
* git config --global user.name "Gemma clavero": asocia mi nombre al user que va a trabajar con este control de versiones
* git confif --global user.email "casagemmayraul@yahoo.es": asocia el email
* git log: Muestra los cambios hechos en la configuracion
* git show <archivo>: Muestra los cambios hechos en ese archivo
* shift zz: te saca de las pantallas raras de git
* No me salen todos los cambio de una. Tengo que ir haciendo enter si el editor tiene una altura muy peque
* git diff <numero larguisimo versionX> <numero larguissimo versionY>: me muestra las diferencias de version
* git reset <numero larguisimo version x> --hard   : Volver a la version vieja (borra todo)
* git reset <numero larguisimo version x> --soft   : Volver a la version vieja pero guradando todo lo posterior
* git diff: Me dice las diferencias entre los archivos en el staging y mi directorio
* Q: Para salir del log?
* git log --stat: Cambios de todos los archivos ?
* git checkout <numero largo> biografy.txt: Me muestra esa version a ver...
* git checkout master biografy.txt: Me muestra la ultima version

## Practica de ramas
* git commit -am: hace commit solo de los archivos que ya se habian hecho commits antes
* Las ramas se cran desde la rama donde yo este ene este momento
* git branch <cabecera> : crea
* git checkout cabecera: Me lleva a rama <cabecera>
* git merge <ramaY>: le fusiona la rama Y que queramos fusionarle... si hay conflictos... ya veremos a la rama en donde estemos

## Practica de uso de SSH
* Me enrede un poco todavia no la tengo clara pero ya tengo clave SSH

## Practica de enlace con repositorio de GitHub
* git remote add origin: 
* git branch -m main: Se cambia el nombre de master a main
* git push origin main
**** Realmente GITHUB lo ayuda a uno ha hacer todos los pasos. **** copi paste





