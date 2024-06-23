PGP (Pretty Good Privacy) **utiliza una combinación de clave pública y cifrado convencional, para proporcionar servicios de seguridad para los mensajes de correo y archivos de datos**.

Primero importamos el archivo .ASC, y segundo desencriptamos el segundo, pero para eso se necesitan credenciales por lo que vamos hacer fuerza bruta con John.

![[Pasted image 20240117201336.png]]

```bash 
pgp --import ARCHIVO.asc
```

# DESENCRIPTAR .PGP

Localizamos primero el gpg2john:
```bash 
locate gpg2john
```

Y pasamos el archivo con otro nombre
```bash 
/usr/sbin/gpg2john tryhackme.asc > john_php
```

![[Pasted image 20240117202026.png]]

Y ahora si pasamos a conseguir dichas credenciales con los siguientes parametros.
```bash
john john_php --wordlist=/usr/share/wordlists/rockyou.txt 
```

![[Pasted image 20240117203121.png]]

ahora si podemos desencriptar el pgp, y tenderemos la desencriptacion lista ya tenemos un usuario que es merlin y una contraseña, que no esta cifrada.
```bash 
gpg -decrypt archivo.pgp
```

![[Pasted image 20240117203448.png]]

Y ya tenemos acceso a Merlin, con la contraseña anteriormente proporcionada.
![[Pasted image 20240117203741.png]]

