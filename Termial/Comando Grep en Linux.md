#Terminal #PinguinoMario #HackingEtico 
Con este comando podemos hacer búsquedas, encontrando líneas donde se encuentra el patrón que estamos buscando, por ejemplo vamos a buscar el nombre Mario dentro del fichero /etc/passwd:
![[Pasted image 20231119181828.png]]
Pero también podemos hacer una búsqueda donde queramos encontrar una cosa o bien otra, por tanto utilizaremos la opción grep -E; y por ejemplo diremos que quiero que me encuentre o bien el nombre Mario o bien el nombre usbmux:
![[Pasted image 20231119181938.png]]
También puedo utilizar este comando pasándole el nombre del archivo donde quiera hacer la búsqueda, por ejemplo puedo buscar todas las coincidencias del nombre Mario en todos los archivos del escritorio, en este caso: grep mario * y vemos que dentro del documento futbol se contiene el nombre de mario:
![[Pasted image 20230128170722.png]]
Si quiero quitar esos mensajes de error, hago lo siguiente, escribo grep -s mario *
![[Pasted image 20230128170826.png]]
#### ELIMINAR UN PATRÓN CON GREP
También podemos hacer que el comando grep nos elimine ciertos elementos de una búsqueda, por ejemplo imaginemos un archivo que tenga muchos elementos que sean la palabra body como este:
![[Pasted image 20230128171248.png]]
Ahora con la opción -v podemos eliminar ese body junto con la línea entera:
![[Pasted image 20230128171320.png]]
Vemos también otro ejemplo donde se elimina la línea completa donde se encuentre situado el nombre de mario:
![[Pasted image 20231119182131.png]]
#### CUÁNTAS LÍNEAS SE REPITE UN PATRÓN CON GREP
También podemos saber en cuántas líneas se repite un patrón utilizando la opción -c, donde en este caso nos dice que la palabra ttl=115 dentro del fichero ping.log se repite una vez, por tanto podemos saber que es un Windows:
![[Pasted image 20230128171531.png]]
Vemos otro ejemplo:
![[Pasted image 20231119182403.png]]