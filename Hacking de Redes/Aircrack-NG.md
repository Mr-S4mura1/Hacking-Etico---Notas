Lo primero será instalar aircrack-ng:
![[Pasted image 20230103115940.png]]
Y ahora es necesario activar el modo monitor en nuestra interfaz de red, fijándonos en el nombre de la interfaz wifi:
![[Pasted image 20230103120115.png]]
Ahora ejecutamos este comando para convertir la antena wifi en modo monitor:
![[Pasted image 20230103120438.png]]
Y ahora si ejecutamos un ifconfig veremos como la interfaz wifi ha cambiado:
![[Pasted image 20230103120719.png]]
Y ahora haremos un escaneo de las redes disponibles con este comando:
![[Pasted image 20230103120946.png]]
![[Pasted image 20230103121047.png]]
Vamos a elegir el wifi llamado Red: 
![[Pasted image 20230103121938.png]]
Y ahora con su BSSID vamos a listar los devices que están conectados a esta red:
![[Pasted image 20230103122905.png]]
![[Pasted image 20230103122931.png]]
Y ahora es cuando tenemos que obtener el handshake; y para ello tenemos que generar tráfico al mismo tiempo, por lo que desde otra ventana vamos a generar tráfico:
![[Pasted image 20230103123344.png]]
Y una vez lanzado esto, ya tenemos el handshake:
![[Pasted image 20230103123418.png]]
Ahora veremos que tenemos una serie de archivos en el actual directorio, que los usaremos más adelante:
![[Pasted image 20230103123555.png]]
Una vez tenemos esto, solo necesitamos ejecutar este otro comando seleccionando el fichero cap:
![[Pasted image 20230103234820.png]]
Y vemos que nos encuentra la contraseña gracias a que se encontraba dentro del diccionario:
![[Pasted image 20230103234902.png]]


