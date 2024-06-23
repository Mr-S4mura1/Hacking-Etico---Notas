#PWN #HackingPython #PinguinoMario #HackingEtico
Para establecer una conexión simple a un equipo por un puerto determinado lo haríamos de la siguiente forma:
```python
from pwn import *

remote('192.168.0.18', 80)
```
Y vemos que la conexión es exitosa:
![[Pasted image 20230417132229.png]]
Incluso se podría probar con un rango de puertos, por ejemplo del 20 al 25:
```python
from pwn import *

for i in range(20, 25):
    try:
        conn = remote('192.168.0.18', i)
    except:
        print(f"Conexión por el puerto {i} fallida")
```
Y vemos el resultado y cómo el 22 está abierto:
![[Pasted image 20230417151230.png]]

--------------------------------------------------
# COMPROBAR SI UN PUERTO ESTÁ ABIERTO
Podemos intentar establecer una conexión con una IP y un puerto para comprobar si se encuentra operativo o no. Por tanto primero creo un servidor web con python desde la máquina de destino:
![[Pasted image 20230417131325.png]]
Y ahora con pwn compruebo la conectividad con este código:
```python
from pwn import *

direccion_ip = '192.168.0.18'
puerto = 80

try:
    remote(direccion_ip, puerto)
    print(f'El puerto {puerto} está abierto en la dirección IP {direccion_ip}')
except:
    print(f'El puerto {puerto} está cerrado en la dirección IP {direccion_ip}')
```
Y si lo ejecutamos, vemos que hay conexión:
![[Pasted image 20230417131404.png]]




