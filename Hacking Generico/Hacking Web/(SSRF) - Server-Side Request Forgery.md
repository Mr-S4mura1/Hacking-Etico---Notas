#HackingWeb #HackingGenerico #PinguinoMario #HackingEtico
Esta vulnerabilidad permite que una aplicación web pueda hacer consultas HTTP del lado del servidor hacia un dominio elegido por el atacante.

-------------------------------------
## Preparar el entorno
Vamos a preparar el entorno con Docker, de tal forma que primero ejecutamos un contenedor de ubuntu:
![[Pasted image 20230706152048.png]]
Y entramos dentro:
![[Pasted image 20230706152110.png]]
Actualizamos los repositorios con un apt update e instalamos apache2, php, nano y python3:
![[Pasted image 20230706153044.png]]
Y ahora habilitamos el servicio de apache con un service apache2 start:
![[Pasted image 20230706153139.png]]
Y tenemos cargada una plantilla de apache:
![[Pasted image 20230706153226.png]]
