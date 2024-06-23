#Red #Herramientas #HackingEtico  

Evil Limite es script el cual nos permite bloquear e limitar el wifi a las personas que se encuentren conectadas a este, el repositorio de este script es: https://github.com/bitbrute/evillimiter

#### Forma de Instalación: 
Esta es la forma de instalación según la información del repositorio:
~~~ bash
git clone https://github.com/bitbrute/evillimiter.git
cd evillimiter
sudo python3 setup.py install
~~~

-----

#### Uso:
La forma de uso de este script es el siguiente, primero necesitamos ejecutar el script el cual ya estará instalado en la terminal y solo basta con poner **evillimiter**, y aparecerá la siguiente información: 

![[Pasted image 20231011190032.png]]

En la opción main existen varios tipos de comandos que se pueden ejecutar, pero en especial voy a hablar de los mas importantes, pero a continuación mostrare todos los comandos posibles __Por si las moscas__. 

![[Pasted image 20231011191807.png]]

Los comandos mas importantes, para empezar a ver quienes están en tu red son 
__scan__ (Este permite escanear todos los dispositivos conectados a la red).

![[Pasted image 20231011192032.png]]
Después de poner el comando scan este nos va a dar una cierta información el cual nos va a decir cuantos dispositivos están conectados a nuestra misma red. Ahora para lograr bloquearlos o ponerles un limite de velocidad son los siguientes comandos.

![[Pasted image 20231011192400.png]]

A continuación lo que estamos haciendo es con el comando __hosts__ viendo todos los dispositivos conectados a nuestra red en este caso solo hay uno, después con el comando __block__ y la IP podemos bloquear a este dispositivo de nuestra red. Para desbloquear al dispositivo solo vamos a requerir del comando __free__ y la IP.

![[Pasted image 20231011192705.png]]

En el caso de que queramos bloquear todos los dispositivos el comando sigue siendo el mismo solo que con  __All__ el comando quedaría de la siguiente forma **Block All**
y para desbloquearlos seria **Free All**. 

Ahora si nosotros queremos es solo ponerle un limite de velocidad el comando seria de la siguiente forma.

![[Pasted image 20231011193518.png]]

En este caso en vez de que coloquemos la IP solo requerimos de colocar el ID del dispositivo conectado Y así es como quedaría Limitado, para dejarlo como antes solo necesitamos es colocar el comando e **Free** mas la IP 