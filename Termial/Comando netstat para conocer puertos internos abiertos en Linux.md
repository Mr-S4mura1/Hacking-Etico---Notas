#Terminal #PinguinoMario #HackingEtico 
Para ver qué servicios están corriendo detrás de un puerto específico en Linux, puedes utilizar el comando netstat y su opción -tulpn. El uso del comando es el siguiente:
```bash
sudo netstat -tulpn
```
Este comando mostrará una lista de todas las conexiones activas en el sistema, incluyendo el protocolo de red (TCP o UDP), la dirección IP local y remota, el puerto local y remoto, y el nombre del programa o proceso que está escuchando en ese puerto:
![[Pasted image 20230211011227.png]]
Para filtrar los resultados y ver solo los servicios corriendo en un puerto específico, puedes utilizar el comando grep junto con netstat:
```bash
sudo netstat -tln | grep :80
```
Y nos encuentra el servicio que está corriendo sobre el puerto 80:
![[Pasted image 20230218141725.png]]

