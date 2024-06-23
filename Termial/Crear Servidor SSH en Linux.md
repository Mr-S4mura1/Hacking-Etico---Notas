#Terminal #PinguinoMario #HackingEtico 
Instalamos openssh-server:
```bash
apt install openssh-server
```
![[Pasted image 20230930100523.png]]
Ahora con el siguiente comando comprobamos que el servicio esté corriendo:
```bash
systemctl status ssh
```
![[Pasted image 20230930100558.png]]
Y ahora podemos entrar vía SSH de forma automática [[Configuración SSH Automático]]
