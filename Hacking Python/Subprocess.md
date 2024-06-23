#HackingPython #PinguinoMario #HackingEtico
Esta librería sirve para interactuar con los procesos de sistema operativo, por ejemplo vamos a ejecutar el comando dir:
```python
import subprocess

comando = "dir" 
resultado = subprocess.run(comando, shell=True)

print(resultado)
```
![[Pasted image 20231012154201.png]]

