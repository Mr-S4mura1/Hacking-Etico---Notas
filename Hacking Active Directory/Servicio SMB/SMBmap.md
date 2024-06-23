#ServiciosSMB #HackingActiveDirectoy #PinguinoMario #HackingEtico 
Smbmap es una herramienta de línea de comandos que se utiliza para enumerar y explorar recursos compartidos en una red SMB.
## Enumerar recursos compartidos en un servidor SMB
```python
smbmap -H <IP address or hostname>
```
Por ejemplo, para enumerar los recursos compartidos en un servidor con la dirección IP 192.168.1.100, puede ejecutar el siguiente comando, el cual mostrará una lista de los recursos compartidos en el servidor, junto con información sobre los permisos de acceso.
```python
smbmap -H 192.168.1.100
```
Y este sería el resultado:
![[Pasted image 20230406074550.png]]
### Enumerar archivos y directorios en un recurso compartido
Podemos enumerar recursos compartidos sin proporcionar credenciales haciendo uso de una null session simplemente usando el parámetro -H:
![[Pasted image 20230420110521.png]]
También podríamos conectarnos haciendo uso de una null session de esta forma:
```bash
smbmap -u "null" -H 10.10.182.108
```
![[Pasted image 20230701103816.png]]
Si quisiéramos proporcionar credenciales, lo haríamos de esta forma:
```python
smbmap -H <IP address or hostname> -u <username> -p <password> -s <sharename> -R
```
Por ejemplo, para enumerar los archivos y directorios en el recurso compartido "compartido1" en un servidor con la dirección IP 192.168.1.100, puede ejecutar el siguiente comando, el cual mostrará una lista de los archivos y directorios en el recurso compartido "compartido1", junto con información sobre los permisos de acceso.
```python
smbmap -H 192.168.1.100 -u usuario -p contrasena -r compartido1
```
![[Pasted image 20230425162011.png]]

--- 
## EJEMPLO FUNCIONAMIENTO SMBMAP

Así sería el funcionamiento de smbmap
![[Pasted image 20230213104857.png]]
# DESCARGAR UN ARCHIVO CON SMBMAP
Lo haríamos con el parámetro --download:
![[Pasted image 20230727151919.png]]

---
# INICIAR SESIÓN DE FORMA NULA 
Para ingresar session de forma nula lo harimaos con los siguiente parametros.
![[Pasted image 20240117145928.png]]

# DESCARGAR RECURSOS CON SMBCLIENT
![[Pasted image 20240117150202.png]]
Esto descargara todos los archivos que se encuntren en dicho directorio.
