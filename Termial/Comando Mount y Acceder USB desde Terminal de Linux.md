#Terminal #PinguinoMario #HackingEtico 
## ACCEDER A PENDRIVE USB DESDE TERMINAL
Al conectarlo, se monta automáticamente en la ruta de la carpeta personal:
![[Pasted image 20230119131936.png]]
## COMANDO MOUNT PARA MONTAR Y DESMONTAR PARTICIONES
Si queremos ver los dispositivos conectados podemos verlo dentro de la ruta /dev con este comando:
![[Pasted image 20230119132103.png]]
Y si queremos expulsar uno de ellos podemos usar el comando umount:
![[Pasted image 20230119132150.png]]
Y ahora podemos montarlo otra vez en la ruta que queramos con el comando mount, pero para ello tenemos que crear una nueva ruta dentro del directorio /media/usb por ejemplo:
![[Pasted image 20230119132716.png]]
Y ahora podemos montar el dispositivo /dev/sdc1 en esta ruta con el comando mount:
![[Pasted image 20230119133001.png]]
Y ya tenemos montado el USB en esta ruta, donde podemos acceder a sus archivos:
![[Pasted image 20230119133058.png]]
Pero para ejecutar el comando mount debemos conocer que sistema de ficheros tiene la unidad USB, ya que en función de eso se ejecuta un comando u otro; estas son las opciones:
![[Pasted image 20230119133212.png]]
![[Pasted image 20230119133223.png]]
![[Pasted image 20230119133234.png]]
Para conocer el sistema de ficheros de una partición o unidad USB usamos el comando df -Th:
![[Pasted image 20230119133502.png]]
