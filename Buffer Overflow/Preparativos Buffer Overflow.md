#BufferOverflow #PinguinoMario #HackingEtico 

Lo primero será tener una máquina windows 7 y la atacante:
![[Pasted image 20230830100218.png]]
Y en la máquina Windows 7 tenemos que descargarnos el servicio vulnerable, llamado SLMail (por ejemplo):
![[Pasted image 20230831111237.png]]
![[Pasted image 20230831111330.png]]
Una vez descargado, antes de instalarlo ejecutamos el siguiente comando:
```powershell
bcdedit.exe /set {current} nx AlwaysOFF
```
![[Pasted image 20230831111906.png]]
Y ahora instalamos el slmail y todo en next:
![[Pasted image 20230831112103.png]]
Incluida esta configuración que también dejaremos por defecto:
![[Pasted image 20230831112212.png]]
