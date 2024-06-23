#Red #Herramientas #HackingEtico 

Lo primero que hago antes de crear el punto de acceso es mirar que tenga la tarjeta de red bien instalada y este modo *Managed*. 

![[Pasted image 20231011203553.png]]

Lo primero ahora es instalar WEF de github y configurarlo, el repositorio de github para ver mas informacion es el siguiente. https://github.com/D3Ext/WEF , para instalarlo es con los siguientes comandos.

``` bash
git clone https://github.com/D3Ext/WEF
cd WEF
bash setup.sh
```

Después de realizar esto, solo basta con escribir en la terminal wef + *nombre de la interface*

![[Pasted image 20231011205315.png]]

![[Pasted image 20231011205613.png]]
Para activar el modo monitor solo basta con colocar *Enable*, después seleccionamos el numero 13 y proseguimos... Cuando termine de cargar todo podemos poner el nombre que nosotros queramos que aparezca como red falsa, y después le pasamos un archivo del sitio a cargar.

