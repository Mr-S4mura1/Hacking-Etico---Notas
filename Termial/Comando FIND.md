#Terminal #PinguinoMario #HackingEtico 
Este comando sirve para encontrar tipos de archivos, por ejemplo vamos a buscar todos los archivos de forma recursiva en mi actual directorio (sólo archivos):
![[Pasted image 20230127070953.png]]
![[Pasted image 20230127071022.png]]
Para buscar un determinado archivo en mi actual directorio con bash lo haría de esta forma:
![[Pasted image 20230127071206.png]]
Incluso con el comando find también podemos indicar que nos haga una búsqueda desde un directorio en concreto, por ejemplo un find desde el directorio raíz buscando en todo el sistema la palabra password:
![[Pasted image 20230210015416.png]]
Y nos encuentra muchos patrones con esta palabra:
![[Pasted image 20230210015440.png]]
También puedo buscar un archivo con un determinado nombre desde la raíz, por ejemplo uno que se llame user.txt:
![[Pasted image 20230507114726.png]]
## SCRIPT PARA AUTOMATIZAR LA BÚSQUEDA DE ARCHIVOS
```bash
#!/bin/bash

# Verificar que se proporcionaron los parámetros adecuados
if [ $# -ne 2 ]; then
    echo "Uso: $0 <ruta> <nombre_archivo>"
    exit 1
fi

# Recoger los parámetros
ruta="$1"
nombre_archivo="$2"

# Buscar el archivo en la ruta especificada
echo "Buscando el archivo '$nombre_archivo' en la ruta '$ruta'..."

# Utilizar el comando 'find' para buscar el archivo
resultado=$(find "$ruta" -name "$nombre_archivo")

# Verificar si se encontraron resultados
if [ -n "$resultado" ]; then
    echo "Se encontraron los siguientes archivos:"
    echo "$resultado"
else
    echo "No se encontraron archivos con el nombre '$nombre_archivo' en la ruta '$ruta'."
fi
```