#HackingActiveDirectoy #PinguinoMario #HackingEtico 
Un servidor HTA se puede utilizar como parte de una carga útil para la explotación de sistemas y la ejecución de código malicioso. Los archivos HTA son una forma de ejecutable que utiliza HTML, JavaScript y VBScript para crear aplicaciones basadas en navegador con acceso a funcionalidades del sistema operativo.

----------------------------

Usamos el siguiente módulo para montar un servidor HTA:
```bash
use exploit/windows/misc/hta_server
```
Y lo ejecutamos, donde vemos que se estará alojando un servidor http:
![[Pasted image 20230801090109.png]]
Si entramos en esta url desde la máquina víctima, vamos a obtener ejecución remota de comandos con una sesión de meterpreter:
![[Pasted image 20230801090149.png]]
![[Pasted image 20230801090201.png]]
