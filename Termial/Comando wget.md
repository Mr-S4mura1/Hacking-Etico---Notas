#Terminal #PinguinoMario #HackingEtico 
`Wget` es una herramienta de línea de comandos utilizada para descargar archivos desde la web. El nombre "wget" proviene de "web get". Este comando es comúnmente utilizado en sistemas basados en Unix y Linux, pero también está disponible para otros sistemas operativos.

-----------------

Por ejemplo, este sería el uso básico:
![[Pasted image 20231119175227.png]]
También podemos descargar un archivo cambiándole el nombre directamente:
```bash
wget -O nombre_cambiado.py https://raw.githubusercontent.com/Maalfer/ReverseShell_Python/main/atacante.py
```
![[Pasted image 20231119175334.png]]
O también descargar varios archivos a la vez:
```bash
wget https://raw.githubusercontent.com/Maalfer/ReverseShell_Python/main/atacante.py https://raw.githubusercontent.com/Maalfer/ReverseShell_Python/main/v%C3%ADctima.py
```
![[Pasted image 20231119175443.png]]
También podemos descargar archivos de forma recursiva, es decir, todos a la vez. Por ejemplo vamos a montar el siguiente servidor HTTP con python:
![[Pasted image 20231211092459.png]]
Y con wget y el parámetro -r nos descargamos todos los archivos, es decir, la opción `-r` activa la descarga recursiva, lo que significa que wget seguirá los enlaces dentro del directorio especificado y descargará archivos en profundidad:
```bash
wget -r http://192.168.0.17
```
![[Pasted image 20231211092528.png]]
Y en nuestro actual directorio se nos habrá creado una carpeta con todos los archivos que estaban alojados en el servidor HTTP:
![[Pasted image 20231211092604.png]]
