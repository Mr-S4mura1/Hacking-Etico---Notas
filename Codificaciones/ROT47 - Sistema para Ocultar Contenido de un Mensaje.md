#Codificaciones #PinguinoMario #HackingEtico 
Podemos utilizar ROT47 en la máquina de vulnhub [[MAQUINA CYBERSPLOIT 2 (Mensajes ocultos con ROT47, acceso por SSH y escalada de privilegios con Docker)]]Y si buscamos por internet esto de ROT47 nos encontramos con que se trata de un cifrado simple que se utiliza para ocultar el contenido de un mensaje; y tenemos herramientas online para descifrar estos mensajes:
![[Pasted image 20230322210657.png]]
Por tanto entramos en la página de rot47.net y podemos probar en poner uno de los textos que nos salía antes en la web:
![[Pasted image 20230322210740.png]]
Pegamos por ejemplo la parte de la derecha en la web:
![[Pasted image 20230322210806.png]]
Y si hacemos clic en ROT47 nos devuelve un usuario shailendra:
![[Pasted image 20230322210828.png]]
Y ahora hacemos lo mismo con el otro dato de la web cybersploit1:
![[Pasted image 20230322210856.png]]
