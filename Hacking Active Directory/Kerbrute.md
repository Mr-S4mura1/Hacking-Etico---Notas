#HackingActiveDirectoy #PinguinoMario #HackingEtico 
Kerbrute es una herramienta para realizar un ataque de fuerza bruta sobre Kerberos en una máquina víctima. Por lo que este es su repositorio:
![[Pasted image 20230425150757.png]]
Y procedemos con su instalación, por lo que en primer lugar lo clonamos y lo instalamos de esta forma, simplemente ejecutando el fichero requirements para que queden instaladas todas las dependencias:
![[Pasted image 20230425150924.png]]
Y con el comando kerbrute ya vemos las instrucciones de cómo utilizarlo:
![[Pasted image 20230425151011.png]]
Ahora tendremos que tener un diccionario de usuarios y otro de contraseñas (que podemos usar los que nos proporcionan en la propia web de tryhackme):
![[Pasted image 20230425154502.png]]
![[Pasted image 20230425154603.png]]
## BÚSQUEDA DE USUARIOS DOMINIO
Y este es el parámetro que debemos usar para hacer una búsqueda de usuarios válidos del dominio:
```bash
python3 kerbrute.py -users userlist.txt -passwords passwordlist.txt -domain spookysec.local -t 100
```
Y en el resultado vemos varios usuarios, aunque hay uno de ellos que no requiere autenticación:
![[Pasted image 20230425154919.png]]
