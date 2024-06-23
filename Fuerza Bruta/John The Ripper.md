#FuerzaBruta #HackingEtico 

Es una herramienta la cual nos permite descifrar contraseñas de usuarios por medio de los hashes, esta es una herramienta especial la cual nos permite descifrar la contraseña por medio de un diccionario el cual es **Rockyou.txt** el cual el un diccionario muy amplio de grandes contraseñas. Rockyou tiene muchas modalidades como la famosa de ssh2john el cual permite descifrar contraseñas privadas de SSH. A continuación la forma de utilizarlo.

#### Descomprimirlo:
Lo primero que debemos de saber es que el diccionario de Rockyou tiene que estar descomprimido para descomprimir el archivo es necesario esta ubicado en la carpeta: */usr/share/wordlist/* y allí encontrar un archivo llamado rockyou.txt.gz, con el siguiente comando podrás descomprimirlo:

```bash
gzip -d rockyou.txt.gz
```

#### Uso:
El modo básico para usar john the ripper es pasando le un archivo y un diccionario con el cual podremos descifrar la contraseña, con el siguiente comando:

```bash
john --wordlist=/usr/share/wordlist/rockyou.txt archivo.txt
```

---------------

#### Ssh2john:
Ahora si nosotros queremos saber las contraseña del archivo de *PrivateKey* de ssh necesitamos primero convertir la contraseña en un hash para poder descifrarla y después con john podremos descifrarla, los comandos a continuación: 

```bash
ssh2john archivo.txt > archivohash.txt
```

Con este comando hemos cambiado la *PrivateKey* a hash para ahora si poder descifrarla, este comando no genera ninguna salida pero, sabremos que todo esta bien si el nombre de archivohash aparece en la carpeta que nos encontremos actualmente.

```bash
john --wordlist=/usr/share/wordlist/rockyou.txt archivohash.txt
```

Y listo con eso ya podremos saber la contraseña de la *PrivateKey*, por lo que ahora ya podremos ingresar por medio de SSH



