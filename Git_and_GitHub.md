La información más útil here.

cat -n [file] | less
	Así buscar desde la Terminal la parte del código que buscamos. 



---

# ¿Por qué usar Git?


## git init: 
	Inicia el repositorio de Git. 
	Crea el directorio .git en el directorio actual. 
---
# ¿Qué es Git?

https://www.notion.so/pogolo/2-Qu-es-Git-d6016153b9084b5aaa43f221e265ad15#98785438f6f3420f83d778f87fb26534


---
# Instalar Git

https://www.notion.so/pogolo/14-Instalando-Git-65ed57e4ec1b4f66ac99e8e681d70b89

---
# ¿Qué es WSL 2? 

Una característica de Windows, un subsistema. Es como un paquete que en su interior trae herramientas del mundo de Linux (el kernel completo de una distribución Linux funcional dentro de Windows, una CLI de Linux)

# Tipos de Texto

## .txt
	Archivo de texto plano, simple. 
## .rtf
	Archivo de texto enriquecido. Muchas cosas se le puede agregar a las letras, NO imagenes. 
## .md
	Archivo de texto simple, pero con markdown un lenguaje simple para personalizar el texto. 

---
# Introducción a la terminal y línea de comandos 

---
# Comandos Básicos en Git

## Comandos

### git status
	El estados de los archivos. 

### git log [file/branch]
	Te muestra donde se ha commited el archivo
	Te muestra los commits de la rama especifica. 

### git rm --cache [file]
	Eiimina cambios de un archivo especifico del staging area. 

Eliminar cosas de *`staged area`*	

## Configurar git
*git config*:Ver toda la configuración que tiene git.

*git config --list*: Ver la configuración por defecto de tu git y las cosas que le faltan.

*git config --list --show-origin*: Ver donde están las configuraciones guardadas.

*git config --global user.name "Name"*: Cambiar el nombre de usuario en Git

*git config --global user.email "email"*: Cambiar nuestro email en Git

---
# Analizar cambios en los archivos con Git

## git show
	Muestra la diferencia entre los últimos commits.

## git diff
>git diff [Commit´s oldest] [Commit's Newer]
Ver la diferencia entre una versión del proyecto y otra. 


>git diff [Commit´s oldest] [Commit's Newer] [file]
Para solo ver las diferencias dentro de un archivo y no de todo el proyecto. 


*Lo de rojo es lo que había antes, lo de verde es lo que hay ahora.*

---

# 10. ¿Qué es staging area?

git rm --cached [file]
	quitar cambios de staging area. 

## Estados de un Archivo

### Untracked
### Staged
### Tracked
### Commited

### 11. 
Apenas iba para esta clase, pero me di cuenta que necesito un proyecto con el cual practicar. 
Tengo que ponerme a practicar a la par con el curso de HTML y CSS.








######Git Reset
git reset --hard
	Borra todo hasta la versión que especificmanete te dirijas 
git reset --mixed
	Borra todo hasta la versión que especificamente te dirijas, pero deja los cambios en el working directory
git reset --soft
	Borra todo hasta la vesión que especificamente te dirijas, pero deja los cambios en el staging area




	












# Git stash
Para guardar tus cambios temporalmente e irte a otro lado.

## git stash save "mensaje"
Guardar los stashes con algún mensaje

### git stash list
Muestra la lista de cambios temporales

### git stash pop
Te muestra el git stash más reciente (el último en crearse) en el ¿staging area?, y por ende este se borra de la lista.
*Ejecutalo donde quieras remotar el trabajo que stashgeaste.*
>Te muestra el stash

## git stash pop stash@{#}
Te muestra el stash especifico para seguir la ejecución del trabajo detenido.


### git stash drop
Borra el stash más recientemente guardado.
>Borra el stash 

### git stash clear
Borrar todos los stashes

---

## LIFO
*L*ast *I*n, *F*irst *O*ut 

El stash más reciente = El último stash en crearse. 
Los más nuevos siempre se les asigna el número 0 y los demás se les va agregando 1 unidad. 


---


## Elegit un stash especifico |  stash@{#}

### git stash drop stash@{#}
Borra un stash especifico. Mediante su índice

### git stash branch [branchName] stash@{n}
Crea una nueva rama con un stash especifico.

---

## Git Stash | Truco
Puedes modificar un archivo tanto como quieras y *regresar a la versión de un ultimo commit como si nada.* Tan solo ejecutando git stash. 















# git commit --amend | Clase 40
Una forma de hacer cambios al commit más reciente sin tener que hacer un nuevo commmit


## Pasos a seguir
1. Haz los cambios que quieras
2. git add . / git add file 
3. git commit -amend
	3.1 Rescribe el mensaje o dejalo así (funciona como con VIM)
4. Verifica los cambios con git log --stat


### Dudas
Sirve para ambas 
A) Modificar el contenido de un commit ?
B) Modificar el nombre de un commit ?
    *git commit --amend -m "newMensagge"*: Renombrar el commit más reciente.

*git commit --amend --no-edit*: Solo modificar el commit y no el mensaje de este. 

Cuando solo quieres agregar nuevos cambios al último commit y no cambiar el nombre de este commit tan solo ejecuta este comando: 

## Caution
Solo se usa para el entorno local. Nunca con un commit en remoto.  
- Por eso solo mencionan que el `último commit` por seguro este ultimo commit aun lo estas trabajando y aun no lo mandas al repo remoto 🧐👌























