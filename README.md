## Comandos de GIt
* git init: Inicializar el programa de control de versiones
* ls -al: Ver los archivos del directorios actual
* code: Abre code en el directorio actual
* git add .: incluye todos los archivos en el dir a la version. Sube al Staging: MEmoria RAM. Estado temporal
* git add <letra> tab : autocompletado
* git rm <biografy.txt> : elimina el archivo <x> del commit.
* git commit -m "mensaje": Deja los archivos incluidos en un limbo con mensaje de version. Sube al repositorio master
* git config --list-show-origin: Me muestra elementos de configuracion necesaria
* git vonfif -l: Tambien muestra los archivos
* git config --global user.name "Gemma clavero": asocia mi nombre al user que va a trabajar con este control de versiones
* git confif --global user.email "casagemmayraul@yahoo.es": asocia el email
* git log: Muestra los cambios hechos en la configuracion
* git show <archivo>: Muestra los cambios hechos en ese archivo
* shift zz o Q: te saca de las pantallas raras de git
* No me salen todos los cambio de una. Tengo que ir haciendo enter si el editor tiene una altura muy peque
* git diff <numero larguisimo versionX> <numero larguissimo versionY>: me muestra las diferencias de version
* git reset <numero larguisimo version x> --hard   : Volver a la version vieja (borra todo)
* git reset <numero larguisimo version x> --soft   : Volver a la version vieja pero guradando todo lo posterior
* git diff: Me dice las diferencias entre los archivos en el staging y mi directorio
* git log --stat: Cambios de todos los archivos ?
* git checkout <numero largo> biografy.txt: Me muestra esa version a ver...
* git checkout master biografy.txt: Me muestra la ultima version

## Practica de fusion de ramas
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
* git pull origin main: code ayuda, pero para bajar cambios manual

# Conflictos de archivos en remoto que no tienen la misma historia (tipo README o .gitignore creados en la nube)
* git pull origin main --allow-unrelated-histories: arreglar los conflictos de falta de histaria comun
* git status para revisar
* git pull origin main: Descargar sin problema

## Varios 
* git log --all --graph --decorate --online: visualizar los commits comprimidos
* git config --global alias.lgr 'log --all --graph --decorate --oneline': crear alias
* git lgr: Ejecuta el alias
* git config --global --unset alias.<alias>: elimina el alias
* git config --global --get-regexp alias: ver los alias existentes

## TAGS : versionar
* git tag -a v0.1 -m 'Ponemos version v0.1 al estado actual del proyecto' 6a24397: definir version a un commit en particular
* git tag: muestra version
* git show-ref --tags: Muestra version pero con el numero laaargo
* git push origin --tags: Sube los tags creados. Luego en el code en el boton de main donde se cambia la rama visible, se puede poner en lugar de rama (branch), una version x.0 en su lugar.
* git tag -d <nombretag>: borrar un tag

## Subir RAMAS al servidor:
* git show-branch --all: ver todas las ramas con sus commits.
* gitk: Abre editor diciente (flujo) Cheverisimo pero todos en CMD
* git branch: muestra todas las ramas
* git checkout <cabecera>: ir a cabecera
* git push origin <cabecera>: me lleva todo a la rama cabecera

## Buenas practicas:
* Hacer siempre > git pull origin main: Antes de cualquier cosa por si en el servidor han habido cambios del equipo
* A main solo se envia lo que estoy seguro que esta listo para produccion
* git clean -f: Borra todos los archivos que no esten indexados en git y que no esten en .gitignore
* git --dry-run: No me acuerdo?

## Gestion de colaboradores
* Colaborators de GitHub y se incluyen los correos, se manda link, etc. Todo desde Github
* Se crean ramas para que cada colaborador haga su trabajo en cada rama
* git merge fooder y git merge heather y si hay conflictos, se resuelven manualito comparando

## PULL Request: Gestionar aportes de no colaboradores oficiales
* git branch -d <rama>: para borrar ramas en local que ya no se van a usar
* git push origin --delete <rama>: para borrar rama remota
* git branch -r: para ver que ramas remotas tenemos disponibles.
* GITHUB: boton Watch: Para ver los cambios de ese proyecto que nos interesa
* GITHUB: boton Fork: Para clonar un cooia del estado actual del repositorio en nuestro local
* GITHUB: boton : Estrella para indicar que me gusta el proyecto y lo sigo.
* cmd: git clone <con URL del repositorio clonado con Fork>
* GITHUB: Despues de subir el cambio a GITHUB En mi clon en GitHUB hago click en New Pull Request
* GITHUB: Se indica con las opciones la rama donde se han hecho los cambios y la rama donde se quiere colaborar con los cambios
* Al dueño del proyecto le llega correo, mensaje en GITHUB, y se enciende la Pull Request. Le dices ok o lo que quieras y haces click en el boton de aceptar merge.
 
## Quedo desactualizado en mi fork en relacion al proyecto original que Forkee. Entonces:
* git remote add upstream <URL proyecto remoto original al que voy a hacer Fork
* git pull upstream main: Copia del upstream al local
* git commit -am "fusion"
* git push origin main Copia a mi version en GITHUB
  la verdad .... no entiendo muy bien todo esto.

## Imagenes asociadas al proyecto y .gitignore
* las imagenes se alojan en la nube y se hacen referencia. No es buena practica subirlas con el proyecto

## Creacion de paginas en GITHUP Pages
* crear un archivo index.html
* llamar a la pagina <loquesea>.github.io
* las alojo en mi cuenta de facebook y funcionan perfect
* creacion de .gitignore para decirle al proyecto que archivos no subir al repositorio

## Editor de MarkDown: 
* https://pandao.github.io/editor.md/en.html

## Cambios temporales
* git stach: Esto guarda los cambios en un nuevo stash y limpia tu área de trabajo.
* git stash list: Para ver todos los stashes almacenados
* git stash pop: Para recuperar los cambios más recientes guardados en el stash
* git stash branch <english-version>: creacion de la rama que va a contener los cambios del stash
* git commit -am 'I speek english': Se pueden subir los cambios del stash a una rama nueva
* git stash drop: Borra todos los cambios hasta el ultimo commit que se hizo

* git cherry-pick <numero7digitos> : me hace merge de solo el commit que he decidido pese a que en la rama pueda haber mas commits posteriores. Mala practica

  


