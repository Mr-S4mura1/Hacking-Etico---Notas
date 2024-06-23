#WIndows #PinguinoMario #HackingEtico 
Nishang es un conjunto de scripts de PowerShell diseñados para pruebas de penetración y operaciones de hacking ético en entornos Windows. Uno de los scripts incluidos en Nishang es `Invoke-PowerShellTcp.ps1`, que permite establecer una conexión de shell inversa a través de PowerShell en Windows:
![[Pasted image 20230313020159.png]]
Vamos a analizar el código del Invoke-PowerShellTcp.ps1, donde vemos en la parte de example una demostración de cómo ejecutar la reverse shell hacia la máquina atacante:
![[Pasted image 20230313020307.png]]
Por tanto copiamos justo esta línea y la pegamos al final del todo para que se pueda ejecutar:
![[Pasted image 20230313020404.png]]
Nos ponemos en escucha con netcat desde la máquina atacante:
![[Pasted image 20230313020431.png]]
Y ejecutamos este código y recibimos la reverse shell:
![[Pasted image 20230313020508.png]]
![[Pasted image 20230313020524.png]]
