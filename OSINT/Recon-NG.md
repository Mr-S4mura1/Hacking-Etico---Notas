#Osint #PinguinoMario #HackingEtico 
Es una herramienta de código abierto y está escrita en Python. Recon-ng se utiliza comúnmente en pruebas de penetración y evaluaciones de seguridad para recopilar información valiosa sobre un objetivo, como direcciones de correo electrónico, nombres de dominio, subdominios, información de red, entre otros.

-----------

![[Pasted image 20231218193149.png]]
Esta herramienta funciona mediante módulos, y si hacemos una búsqueda, vemos que no nos encuentra ninguno ya que no están instalados:
```bash
modules search
```
![[Pasted image 20231218193256.png]]
Por lo que tenemos que instalar módulos desde marketplace:
![[Pasted image 20231218193331.png]]
Y los podemos buscar mediante el comando:
```bash
marketplace search
```
![[Pasted image 20231218193415.png]]
Por ejemplo, podemos buscar qué hace cada módulo; y en este caso seleccionamos uno de ellos:
```bash
marketplace info discovery/info_disclosure/interesting_files
```
![[Pasted image 20231218193546.png]]
Ahora podemos visualizar e instalar este módulo con el siguiente comando:
```bash
marketplace install discovery/info_disclosure/interesting_files
```
![[Pasted image 20231218193643.png]]
Y con el comando modules search lo podemos ver:
![[Pasted image 20231218193718.png]]
Lo cargamos de la siguiente forma:
```bash
modules load discovery/info_disclosure/interesting_files
```
![[Pasted image 20231218193752.png]]
