Se me ocurrio una mejor idea, tener a ambos archivos dentro del mismo repositorio 


Git 
	Progrma inventado por Linus Torvalds, mismo x de Linux


git init: Inicia el repositorio de Git & Crea el directorio .git
git add: Manda los cambios a staging area
git commit -m "mensaje": Guarda los cambios 

----

######Estados de un Archivo

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


######Git rm

Esto es un comando que borra archivos y nada más que eso.


######Git Reset HEAD
Funciona similar a git rm --cached

Quita los cambios que este guardados en el area de staging, pero los deja en el working directory. 



######Git Merge

Te tienes que ubicar el la rama "principal" (la que quieres que se "coma" a la otra rama), después de eso ejecuta: 


RECUERDA: Esta en la rama "Principal"
Sintaxis 
	git merge [branchSecond]

Al hacer git merge se creará un nuevo commit
La rama fusionada, embebida en otra seguirá ahí, quieta en el tiempo.





#######


####Cambiar de nombre a una rama
git branch -m master main
git branch -m [branchName] [newBranchName]

	
