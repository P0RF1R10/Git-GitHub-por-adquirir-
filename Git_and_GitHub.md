# La información más útil here.

cat -n [file] | less
	Así buscar desde la Terminal la parte del código que buscamos. 

## Cambiar de nombre a una rama
Estás en la rama a la que quieres cambiarle el nombre
Ejecuta: `git branch -m "newName"`

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








###### Git Reset
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



# Repositorio Remoto | Clase 18 ... 22

En el home ejecuta: 
	- sudo apt update	
- ssh-keygen -t ed25519 -C "your email in GitHub@gmail.com"

- eval "$(ssh-agent -s)"

- [ssh-add] [ruta-de-la-llave-privada]
---

- Crea un nuevo repositorio remoto: https://www.notion.so/pogolo/15-Vincular-la-llave-SSH-8bdf5b05a85245b5935d7f8edb92c8ed?pvs=4#705c54aede4c49498f62b519a5193969
https://www.notion.so/pogolo/20-Uso-de-GitHub-996047e1e60944b7aa4bef19f4d07979?pvs=4#b92813053c8249ed9d357f1821c4112d

- Verifica con git remote = `origin` o git remote -v =`push fetch`

- git push origin main
- git pull origin main
- git pull origin main --allow-unrelated-histories
- Ahora si viene el bueno: `git push origin main`



## Cómo proceder cuando el cambio viene de Remoto o Local

> Antes de hacer un push, hacer un pull.

### Remoto => Local
En el repo local (Terminal) ejecuta el comando `git pull origin main`

Tanto local como remoto ahora son iguales. 
### Local => Remoto
El cambio que hagas en local, antes de hacer `git commit`
- git pull origin main 
	Estar actualizado
- git commit -m "bla, bla, bla"
- git pull origin main 
	Por si volvieron a actualizar en remoto 
- Y ahora sí ejecuta: `git push origin main`

> Todo este embrollo es para cuando trabajas en equipo. 


---

Tanto pinche esfuezo para que salga esta mmda: 
> `git@github.com: Permission denied (publickey).
> fatal: Could not read from remote repository.

> Please make sure you have the correct access rights
> and the repository exists.`


## Empezar con HTTPS
- Crea tu repositorio remoto en GitHub
- Copia el link HTTPS
- git remote set-url origin [link HTTPS]
- git remote -v    | git remote 
	Para comprobar debe saler sentencias con las palabras de fetch y push
	o solo origin 

En GitHub
- Ve a la derecha superior (Donde esta tu foto) > Settings > Developer Settings > Personal access tokens > Fine-grained tokens > Generate new token >

- Saldra un pagina para personalizar `lo importante aquí es: Elegir que solo sea para el repo espec & Habilitar todos los permismos 
- Generar token
- Guarda la contraseña/sentencia rara/ porque nunca más la volveras a ver.

- Ahora sí: git pull origin main
	Username & Password


---
# SOLUCIÓN
Cambiar a HTTPS en lugar de SSH
A la hora de crear el token habilita todos los perimisos para ese repositorio de gitHub en especifico. 

- Ejecuta `git remote set-url origin [link HTTPS]`
	Sale en el repositorio remoto en GitHub (el boton verde)

- git pull origin main
	Te pedirá User y password. 
		El user puede ser tu username de GitHub / tu email (al parecer)
		El password 
Tienes que crear un token 
	A la derecha superior (Donde esta tu foto) > Settings > Developer Settings > Personal access tokens > Fine-grained tokens > Generate new token >
	Saldra un pagina para personalizar `lo importante aquí es: Elegir que solo sea para el repo espec & Habilitar todos los permismos (No se que permiso hizo que si se aceptara la contraseña) 
	No se que cosa si no se habilida no se acepta la contraseña
- Generar token
- Guarda la contraseña/sentencia rara/ porque nunca más la volveras a ver.

- Ahora sí: git pull origin main
	Username & Password





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























