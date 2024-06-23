#Terminal #PinguinoMario #HackingEtico 
**Configurar IP estática**
Primero configuramos la IP estática editando el fichero /etc/netplan/00-installer-config-yaml o 50-cloud-init-yaml (el que encontremos) y estableciendo la IP y demás ajustes que queramos:
```bash
network:
  version: 2
  renderer: networkd
  wifis:
    wlan0:
      dhcp4: no
      addresses: [192.168.0.25/24]
      gateway4: 192.168.0.1
      nameservers:
        addresses: [8.8.8.8, 8.8.4.4]
```
![[Pasted image 20231221160105.png]]
Y ahora aplicamos estos cambios con el comando netplan apply:
```bash
sudo netplan apply
```
**Instalación de Servidor FTP**
Y ahora instalamos vsftpd:
```bash
apt install vsftpd
```
Y ahora iniciamos el servicio:
```bash
systemctl start vsftpd
systemctl enable vsftpd
systemctl status vsftpd
```
![[Pasted image 20231221152906.png]]
Una vez hecho esto, probamos la configuración accediendo desde otro PC con las credenciales que usamos para loguearnos con el usuario mario o el que corresponda:
![[Pasted image 20231221153018.png]]
**Enjaular Usuarios FTP**
Pero tenemos el problema de que este usuario puede navegar por los directorios, y lo que debemos hacer es que este usuario solo pueda estar en su directorio /home:
![[Pasted image 20231221153103.png]]
Por lo que editamos el fichero de configuración de vsftpd, el cual si le quitamos los comentarios viene así por defecto:
![[Pasted image 20231221153301.png]]
Por lo que añadimos estas 2 líneas. La primera es para establecer un directorio donde cada usuario tendrá su configuración: y la otra es para hacer que cada usuario se encuentre enjaulado en su directorio:
```bash
chroot_local_user=YES
allow_writeable_chroot=YES
write_enable=YES
```
![[Pasted image 20231221164138.png]]
Y reiniciamos el servicio:
```bash
systemctl restart vsftpd
```
Y vemos que se configuró correctamente:
![[Pasted image 20231221153915.png]]
Y ahora si entramos como mario vemos que este usuario se encuentra enjaulado en su directorio:
![[Pasted image 20231221155339.png]]
Lo mismo podemos hacer con cualquier otro usuario, por lo que creamos otro usuario y vemos que funcionará igual:
```bash
adduser pepe
```
![[Pasted image 20231221155530.png]]
Y lo mismo pasará si entramos como este usuario vía FTP, que también estará enjaulado:
![[Pasted image 20231221155628.png]]




