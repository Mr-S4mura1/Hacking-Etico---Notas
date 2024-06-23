#Terminal #PinguinoMario #HackingEtico 
El proceso general es el siguiente:

1. Tú generas un par de claves (pública y privada) y mantienes la clave privada en secreto.
2. La persona destinataria también genera su par de claves (pública y privada) y te envía su clave pública.
3. Cuando quieras enviarle un archivo cifrado, utilizas su clave pública para cifrar el archivo. Solo la persona destinataria podrá descifrarlo con su clave privada.
4. La persona destinataria utiliza su clave privada para descifrar el archivo.

---------------------------------

En primer lugar, voy a utilizar dos máquinas virtuales, donde una será mi máquina ubuntu donde recibiré el documento encriptado; y la otra un Kali Linux, que será la que creará un documento que se enviará de forma encriptada a la máquina Ubuntu. Por tanto, en primer lugar vamos a crear un par de claves RSA en cada una de esta máquinas con el comando gpg –gen-key:
![[image6.png]]
Después se nos pedirá que introduzcamos una contraseña:
![[image7.jpeg]]
Y ahora debemos exportar la clave pública a un fichero de esta manera:
![[image8.jpeg]]
Ahora vamos a enviar esta clave pública al equipo Kali Linux:
![[image9.jpeg]]
Crearemos el fichero sad22.txt que será el fichero que vamos a encriptar y enviar a la máquina Ubuntu:
![[dgdfghdfghdfg.png]]
Importamos la clave pública generada desde Ubuntu a nuestro Kali:
![[image11.jpeg]]
Y ahora encriptamos el fichero desde mi máquina Kali Linux:
![[image12.jpeg]]
En este punto ya podremos enviar el fichero encriptado a la máquina Ubuntu para desencriptarlo con la clave privada generada al principio con la máquina Ubuntu; y gracias a que la clave privada ya existe en esta máquina, podremos desencriptar el archivo:
![[image13.jpeg]]
Y ya tendremos el archivo desencriptado:
![[image14.jpeg]]
Por último, voy a listar las claves generadas de ambas máquinas con el comando gpg -k:
![[image15.png]]
![[image16.jpeg]]
