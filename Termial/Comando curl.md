#Terminal #PinguinoMario #HackingEtico 
`curl` es una herramienta de línea de comandos que se utiliza para realizar solicitudes de transferencia de datos a través de diversos protocolos de red. Su nombre es una abreviatura de "Client for URLs" (Cliente para URLs). La función principal de `curl` es transferir datos con URL:

Algunos de los protocolos que `curl` admite incluyen:

1. **HTTP y HTTPS:** Para acceder y transferir datos desde y hacia servidores web.
2. **FTP:** Para la transferencia de archivos a través del protocolo FTP (File Transfer Protocol).
3. **SCP y SFTP:** Para la transferencia segura de archivos sobre SSH.
4. **LDAP:** Para acceder a directorios y servicios de directorio.
5. **IMAP y POP3:** Para acceder a correos electrónicos a través de los protocolos IMAP (Internet Message Access Protocol) y POP3 (Post Office Protocol 3).
6. **SMTP:** Para enviar correos electrónicos a través del protocolo SMTP (Simple Mail Transfer Protocol).
7. **DNS:** Para realizar consultas DNS y obtener información sobre nombres de dominio.

Por ejemplo, este comando realizará una solicitud GET a la URL proporcionada y mostrará la respuesta en la salida estándar:
![[Pasted image 20231119174449.png]]
### DESCARGAR ARCHIVOS CON CURL
Si queremos descargar un archivo con curl, utilizamos el parámetro -o de la siguiente forma por ejemplo ante un archivo de github donde tengamos visión de raw:
```bash
curl https://raw.githubusercontent.com/Maalfer/ReverseShell_Python/main/atacante.py -o atacante.py
```
![[Pasted image 20231119174646.png]]
### VERIFICAR CÓDIGO DE ESTADO CON CURL
Podemos comprobar si una petición se ha llevado correctamente o no, utilizando curl con los siguientes parámetros:

- `-s` significa "modo silencioso" y se utiliza para hacer que curl no muestre mensajes de progreso ni mensajes de error durante la transferencia de datos.
- `-o` se utiliza para especificar el archivo de salida donde se guardará la salida de la solicitud HTTP.
- `-w` se utiliza para especificar el formato de salida que se desea mostrar después de que se haya completado la transferencia de datos. En tu comando, se utiliza `-w "%{http_code}\n"`, lo que significa que solo se imprimirá el código de estado HTTP seguido por un salto de línea.

```bash
curl -s -o /dev/null -w "%{http_code}\n" https://www.google.com/
```
![[Pasted image 20231119174930.png]]
