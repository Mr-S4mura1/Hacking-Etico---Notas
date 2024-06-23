#Terminal #PinguinoMario #HackingEtico 
## Para descargar archivos del servidor
Lo haremos con scp utilizando este comando, primero poniendo la IP del servidor desde donde queremos bajarnos el archivo, y luego la ruta de nuestra máquina local donde lo queramos descargar:
![[Pasted image 20230119184948.png]]
## Para subir archivos al servidor
Vamos a subir este archivo:
![[Pasted image 20230119185202.png]]
Para ello ejecutamos el siguiente comando:
![[Pasted image 20230119185251.png]]
Y ya lo tenemos subido:
![[Pasted image 20230119185308.png]]
## Para subir una carpeta entera por SSH
Si queremos subir todos los archivos que estén dentro de una carpeta, lo haríamos de esta forma; aquí tenemos la carpeta:
![[Pasted image 20230119185522.png]]
Y con este comando lo subiríamos todo, ya que con el asterisco indicamos que suba la totalidad de archivos, y con la opción -r que sea recursivo:
![[Pasted image 20230119190046.png]]
Y aquí están:
![[Pasted image 20230119190103.png]]

# PASAR ARCHIVOS POR SCP CON DIFERENTE PUERTO

Para cambiar el puerto al enviar archivos por SCP tenemos que agregar el parametro -P
![[Pasted image 20240117192717.png]]
