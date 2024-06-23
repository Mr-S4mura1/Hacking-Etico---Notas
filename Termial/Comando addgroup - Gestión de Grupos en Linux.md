#Terminal #PinguinoMario #HackingEtico 
Podemos crear un grupo y ahí meter un determinado usuario:
```bash
sudo addgroup empleados
```
Y si visualizamos el fichero groups podremos ver todos los grupos creados en el sistema:
![[Pasted image 20231119172900.png]]
A continuación, si queremos añadir usuarios a este grupo lo hacemos con el comando usermod de la siguiente forma:
```bash
sudo usermod -aG empleados esteban
```
Y así alñadimos a esteban al grupo empleados y también podemos ver con el comando getent los usuarios que están dentro de un grupo:
![[Pasted image 20231215103231.png]]
A continuación, para gestionar permisos de grupos, vamos a crear un documento.txt y haremos que los usuarios del grupo empleados no puedan ver el contenido de este documento:
![[Pasted image 20231215103319.png]]
Donde hacemos la prueba y vemos cómo ahora este archivo no tiene ningún permiso para los grupos:
![[Pasted image 20231215103426.png]]
Por lo que ahora, cambiamos el grupo dueño del archivo de mario a empleados:
```bash
sudo chown :empleados documento.txt
```
![[Pasted image 20231215103532.png]]
Y vemos que esteban, al formar parte del grupo empleados, no puede visualizar ni hacer nada con el documento:
![[Pasted image 20231215103614.png]]
En cambio Pepe sí que puede visualizar el documento, porque no se encuentra dentro del grupo empleados y por tanto este usuario se considera 'otros':
![[Pasted image 20231215103715.png]]
Ahora vamos a meter a Pepe en el grupo de empleados y veremos cómo no podrá visualizar el documento:
![[Pasted image 20231215103815.png]]