#Terminal #PinguinoMario #HackingEtico 
Para crear un usuario, utilizamos el siguiente comando:
```
adduser pepe
```
![[Pasted image 20231119172220.png]]
Y vemos que el usuario se ha creado correctamente:
![[Pasted image 20231119172246.png]]
Y con el comando su pepe podemos convertirnos en dicho usuario:
![[Pasted image 20231119172528.png]]
Y también podemos visualizar el fichero /etc/passwd para comprobar la existencia de este usuario:
![[Pasted image 20231119173430.png]]
### ELIMINAR UN USUARIO EN LINUX
Para eliminar un usuario, usamos el comando deluser de la siguiente forma:
```
sudo pkill -9 -u pepe # Detenemos los procesos que esté usando el usuario.
deluser --remove-home pepe
```
![[Pasted image 20231119173932.png]]
