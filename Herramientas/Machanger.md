#Herramientas #HackingEtico  

*Machanger* es una aplicacion la cual nos permite cambiar la mac de nuestros dispositivos, esto nos sirve por ejemplo cuando nos bloquean en una red wifi y impiden que cierta mac se pueda conectar pues con machanger podremos cambiarla. A continuacion su modo de uso.

#### Instalacion:
Primero para poder instalar esta herramienta requerimos del siguiente comando. 

```bash
sudo apt install macchanger macchanger-gtk
```

Después de instalar tenemos que conocer nuestra mac para conocerla solo basta con el comando *ifconfig wlan0* y allí nos aparecerá nuestra mac, después de eso podemos proceder a el modo de Uso

![[Pasted image 20231020164103.png]]

------

#### Uso 
Lo primero que tenemos que hacer es desactivar nuestra interfaz de red para eso lo podremos hacer con el comando *sudo ifconfig wlan0 down* después de darle de baja a nuestra interfaz de red podemos proceder a cambiarla, el comando es:

```bash
macchanger -r wlan0 # La cambia aleatoriamente
macchanger -e wlan0 # Registrarse con el mismo proveedor
macchanger --mac = xx:xx:xx:xx:xx:xx # xx es a la mac que desea cambiar
macchanger -p wlan0 # cambiar la mac al valor original y permanente
```

Para que podamos volver a habilitar nuestra tarjeta de red solo basta con el comando *sudo ifconfig wlan0 up*, y listo con eso hemos cambiado la mac de nuestro dispositivo
