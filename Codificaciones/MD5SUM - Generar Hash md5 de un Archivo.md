#Codificaciones #PinguinoMario #HackingEtico 
El comando "md5sum" es una herramienta de línea de comando que se utiliza para generar el valor hash MD5 de un archivo. Se utiliza de la siguiente forma:
![[Pasted image 20230316213042.png]]
También podríamos automatizar esta labor y crear un script de bash que recorra cada uno de los archivos de un directorio y reporte el hash de cada uno de ellos:
```bash
#!/bin/bash

# Obtener la lista de archivos en el directorio actual
files=$(ls)

# Recorrer cada archivo utilizando un bucle for
for file in $files; do
  md5sum $file
done
```
![[Pasted image 20230523153112.png]]
Aunque esto mismo también se podía haber hecho directamente desde la línea de comandos de la siguiente forma:
```bash
variable=$(ls); for file in $variable; do echo $file; done
```
![[Pasted image 20230523153344.png]]