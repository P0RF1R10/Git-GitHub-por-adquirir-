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
# 























# Estados de un Archivo

####Untracked
Unstaged
Tracked
Staged
Commited


Secciones del Flujo de Trabajo con Git

Working directory

Staging Area

Repositorio | Directorio .git


######Git Reset
git reset --hard
	Borra todo hasta la versión que especificmanete te dirijas 
git reset --mixed
	Borra todo hasta la versión que especificamente te dirijas, pero deja los cambios en el working directory
git reset --soft
	Borra todo hasta la vesión que especificamente te dirijas, pero deja los cambios en el staging area




	
