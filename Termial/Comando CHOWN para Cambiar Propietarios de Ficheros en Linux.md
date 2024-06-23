#Terminal #PinguinoMario #HackingEtico 
En Linux, el comando `chown` se utiliza para cambiar el propietario de un archivo o directorio. Para cambiar el propietario de un archivo, se hace de la siguiente forma:
```bash
sudo chown nuevo_propietario archivo
```
Por tanto, por ejemplo tenemos este archivo de python:
![[Pasted image 20230216164054.png]]
Y ahora vemos que el propietario de este archivo pasa a ser mario:
![[Pasted image 20230216164120.png]]
Hay que entender que el nombre de la izquierda es el usuario propietario y el nombre de la derecha el grupo:
```bash
-rw-r--r-- 1 usuario grupo  25 Feb 16 15:30 archivo.txt
```
