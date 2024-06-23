#Osint #PinguinoMario #HackingEtico 
Podemos usar estos comandos para encontrar información de un dominio, por ejemplo la IP, donde veremos en el siguiente caso que hay 2 direcciones IP, pero es porque se utiliza un proxy (cloudflare):
![[Pasted image 20230726110838.png]]
# ROBOTS.TXT
Y esta web tiene el robots.txt habilitado, lo que significa que aquí se ponen las entradas que queramos o no queramos que google indexe en su navegador, por lo que puede ser muy útil para detectar información sensible:
![[Pasted image 20230726111054.png]]
# COMANDO WHOIS
Con este comando podemos obtener mucha información de un dominio. Su función principal es proporcionar datos de registro y contacto relacionados con el propietario, el registrador, el servidor de nombres y otra información relevante sobre el recurso de red consultado:
![[Pasted image 20230726111609.png]]
# DNSRECON
Su función principal es obtener información útil sobre la infraestructura de DNS de un objetivo, lo que puede ser valioso para identificar posibles vulnerabilidades o configuraciones incorrectas que puedan ser explotadas:
![[Pasted image 20230726112022.png]]
Aunque también tenemos la web de dnsdumpster que es ideal para obtener una información más ordenada y detallada:
https://dnsdumpster.com/
![[Pasted image 20230726112210.png]]
