#Terminal #PinguinoMario #HackingEtico 
Podemos comprobar si un fichero existe o no utilizando el comando test -f de esta forma:
```bash
#!/bin/bash

# Verificar si el archivo script_bellisimo.py existe y es un archivo regular

if test -f script_bellisimo.py; then
  echo "El archivo existe"
else
  echo "El archivo no existe"
fi
```
Y este es el resultado:
![[Pasted image 20230211021925.png]]
