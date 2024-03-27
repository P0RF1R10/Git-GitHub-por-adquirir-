RECUERDA: 
>LA MAYORÍA DE ESTAS COSAS SE PUEDEN COMBINAR
>SOLO ANOTA LAS COSAS QUE AÚN NO SE APRENDES, NO PIERDAS TIEMPO ESCRIBIENDO LO MISMO ALWAYS.



####Flags (Que en la mayoría de los casos son compatible)
	-r; Recursivo: Recomendado para directorio
	flag; NameFlag:...


######Primeros pasos en la Terminal

cp; Copiar un archivo
	cp [fileACopiar] [newNamefilepirata]
	

cat [file]; Muestra el contenido del archivo. 
cat [file1] [file2]; Se puede hacer con más archivos al mismo tiempo. 
cat -b: Cuenta y muestra las líneas del archivo **con contenido**.


#file
file [file]; Da una breve explicación del tipo de archivo.

######Herramientas de la Terminal

#####explorer.exe:
	Para abrir el Explorador de Archivos de Windows (EAW) 
#####code:
	Para abrir VSC desde la Terminal
#####wslview:
	Una combinación de ambos.

find: Creo que es un comando que se usa junto con los wildcards
        ejemplo: find *.js
 

######¿Qué es un Comando?

#####Un Comando de Utilidad de la Shell:
- Al escribir type saldrá: **Z is a shell builtin**
- Son extranjeros, externas.

#####Una Función de la Shell:
- Al escribir type saldrá: **X is /Usr/bin/X**
>Z es un shell integrado, incorporado, ...
- Son nativos, internas.


#####Un programa ejecutable
	Un binario, un programa. 
	La mayoría estan en la ruta /User/Bin	

#####Un alias


####type
Un Comando de Utilidad de la Shell

Comando que sirve para identificar que tipo de comando son otros (solo sirve para Un Comando de Utilidad de la Shell, Una Función de la Shell, Un Alias)
Gracias a <type> es posible indentificar si una Función de la Shell, Un comando de Utilidad de la Shell, Un alias.


>file: Para saber que tipo de archivo es.
>type: Para averiguar cual de los 3 posibles "tipos de comando" es uno.

> ~~Aún no se como saber como identificar un binario~~


#####Anatomía de Un Comando
[Comando] [opciones] [Argumentos]
  [cat]      [-b]   [historia.txt]

Comando; Nombre con el que se invoca el comando.

flags;Que modifican el comportamiento del comando. (Son opcionales).

Argumentos; Sobre los que actúa el comando. (También opcionales).


######Wildcards
>Serie de patrones o Caracteres especiales que permiten hacer búsquedas avanzadas.

#####ls *
Enlistará algo que tenga delante o atrás del asterisco. 

#####









#Comandos de Ayuda

man: El manual del comando. 
help: Ideal para los Comandos de Utilidad de la Shell. Sometimes "run-help"
info: Descripción del comando. 
whatis: Una descripción de una sola línea. 













#*Wildcards*

Los wildcards buscan hasta en 2 niveles. 
-d: Flag para solo hacer busquedás en el mismo nivel.

Son los siguientes *, ?, [], [[:clase:]]

*: Para todo caracter alfanúmerico Que inicie con (star*) o Que termine con (*end) & Que inicie con tal y que termine con tal (star*end)

?: Bueno para buscar palabras que terminen similares y al final cambien un poco (ls *a????) = ardilla.css mana.txt reloja.css

[]: 1.Busca entre todas sus opciones [1,5] 1 o 5  2.Busca dentro de un rango [1-4] 1, 2, 3, 4









######Comando WC

LoWoMoCo | Acronimo + o's

Al ejecutarlo en un archivo (en carpetas no va bien) nos da tres cantidades; *Líneas llenas o vacías*, *cantidad de caracteres alfanúmericos*, *peso de caracteres en bytes* respectivamente.

*-c*; (--bytes)
     Print only the byte counts.

*-m*; (--chars)
     Print only the character counts.

*-w* (--words)
     Print only the word counts.

*-l* (--lines)
	Print only the newline counts.



repeat # {acción}:
	De este modo podemos repetir una acción n cantidad de veces












######Operadores de Control
   INCONDICIONALES

	&: Asincrono. Se ejcutan de forma paralela. 
	; Sincrono. Ejecuta uno tras el otro de forma secuencial
   CONDICIONALES 

	&&: Ejecuta todos de forma paralela
	||: Con que uno se ejecute ya chingo.














######Permisos de Archivos
Nos enfocaremos en el Usuario Owner                Terminal, VSC, EAW

-RWX          ARCHIVO -        CARPETA D










######Enlaces Simbolicos

Así se crean: 
	ln -s [rutaAbsoluta] [NameEnlaceSimbolico]
Delete
	rm [linkSimbolicoName]






######Agregar Binarios a Path

PATH=$PATH:[RUTA DEL BINARIO]
path es igual al path acutal y agrega este nuevo programa, ruta, binario




######FIND

find (ruta) (segmentos [opciones]) (a wildcard)




Marzo 17 2024 
 
######Sobre VIM & VI.

- Bueno para escribir solo se usar la tecla I
- Para entrar en modo Normal se usar Esc or Ctrl + C
- Para entrar a modo interactivo solo se usa la Tecla I

- Usando / en el modo Normal podemos buscar la 1° coindidencia, nada más.





.

vimtutor para ver un tutorial de ello.



Solo quiero ver si desde un Link Simbolico puedo hacer cambios y que se reflejen en el archivo original (que ya esta en un repositorio de Git)

