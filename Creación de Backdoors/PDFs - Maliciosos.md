#CreacionBackdoors #HackingEtico 

Creamos un backdoor con *msfvenom* normal, como siempre el pyload a ultilizar es: *windows/meterpreter/reverse_tcp*, mas informacion en el siguiente archivo de como crear este backdoor. 

![[Creacion de Malware con Metasploit - Windows]]

Antes proceder a ponernos por escucha en *msfconsole* vamos a convertirlo en PDF para enviarlo a nuestras victimas. Para eso vamos a ultilizar Winrar y para poder armar nuestro PDF necesitamos obligatoria mente los siguientes herramientas.

- PDF
- Malware
- Icon (PDF)

Despues de eso vamos a seleccionar el malware y el pdf y le vamos a colocar cualquier nombre en este caso voy a colocar importante.pdf

![[Pasted image 20240114213300.png]]

Seleccionamos método de extraccion autoextraible y seleccionamos compresión la Mejor.
![[Pasted image 20240114213519.png]]

Vamos ahora a la pestaña avanzado, opción autoextraible y opción Instalacion
y allí en el campo de *Ejecutar tras la extraccion* el nombre de el *PDF* y del *Malware*

![[Pasted image 20240114213906.png]]

Y ahora vamos a cambiar el *ICONO* para eso vamos a la pestaña *Texto e Icono*, seleccionamos nuestro icono y listo ya todo estario OK, ahora solo quedaria enviarselo a nuestra victima.

