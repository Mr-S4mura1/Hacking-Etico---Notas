#Terminal #PinguinoMario #HackingEtico 
Este comando sirve para obtener información de un archivo, así como lo que ocupa; y esta es su sintaxis básica:
```bash
du -h user.txt
```
![[Pasted image 20230922125502.png]]
Podemos formatear con regex el tamaño de un archivo de esta forma:
```bash
tamaño=$(du -h user.txt | awk '{print $1}')
echo "El archivo user.txt ocupa $tamaño"
```
![[Pasted image 20230922125737.png]]