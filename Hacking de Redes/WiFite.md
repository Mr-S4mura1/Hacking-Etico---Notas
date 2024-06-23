#Red #Herramientas #HackingEtico 

Esta es una herramienta que es para Auditar Redes, permite auditar redes inalambricas de manera automática, su modo de instalación es el siguiente:

```bash
sudo apt install wifite
```

y ahora para que podamos empezar a utilizarlo solo necesitamos ejecutar el la terminal el comando de **wifite** y empezara a ejecutarse el programa, este nos va a pedir unos ciertos requerimientos que es necesario tenerlos instalados.

+ **Pyrit:** Permite utilizar ciertos parámetros para realizar evaluación de redes inalambricas en pocas palabras ataques de *Contraseñas*
+ **Hcxdumptool**: Funciona para Ataques PMKID 
+ **Hcxcapngtool**: Funciona para Ataques PMKID 

![[Pasted image 20231012123616.png]]

Para instalar pyrit se requiere del siguiente repositorio, a continuación esta todo el comando para que se clone a la perfección.

```bash
git clone https://github.com/hacker3983/pyrit-installer && cd pyrit-installer && sudo bash install.sh
```

Instalar Hcxdumptool

```bash
sudo git clone https://github.com/ZerBea/hcxdumptool.git && cd hcxdumptool && sudo make && sudo make install
```

Instalar Hcxcapntool

```bash
sudo git clone https://github.com/ZerBea/hcxtools.git && cd hcxtools $$ sudo make && sudo make install
```

Procedemos a ejecutar ahora si el programa con el comando **wifite** y le tenemos que pasar un diccionario con el parámetro *--dict + file*, después de ejecutar el comando se estarán mostrando por pantalla algunas redes.

![[Pasted image 20231012130015.png]]
Cuando detectamos la red a la cual queremos realizar el ataque *PMKID* tecleamos ctrl+c
y ingresamos por pantalla el numero de esa red.

![[Pasted image 20231012130339.png]]

Lo bueno de tener esta aplicación es que con solo ejecutarla te captura por si sola el handshake y te hacer fuerza bruta por diccionario para encontrar la contraseña.