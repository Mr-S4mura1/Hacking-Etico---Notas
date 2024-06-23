#Osint #PinguinoMario #HackingEtico 
Esta es la herramienta:
![[Pasted image 20231218183557.png]]
Por ejemplo, podemos hacer una búsqueda sencilla de la siguiente forma:
```bash
theHarvester -d microsoft.com -b bing -l 100
```
Donde:
1. **-d:** Este parámetro especifica el dominio objetivo sobre el cual se realizará la recopilación de información. theHarvester buscará información asociada con este dominio.
    
2. **-b bing:** Este parámetro especifica el motor de búsqueda que theHarvester utilizará para realizar la búsqueda de información. En este caso, se ha seleccionado "bing" como el motor de búsqueda. theHarvester puede utilizar diferentes motores de búsqueda, como Google, Bing, PGP, LinkedIn, etc. Cada motor de búsqueda tiene su propia base de datos y métodos de búsqueda, por lo que el resultado puede variar según el motor seleccionado.
    
3. **-l 100:** Este parámetro indica el límite de resultados que se deben recuperar. En este caso, se ha establecido en 100, lo que significa que theHarvester intentará recuperar hasta 100 resultados.

![[Pasted image 20231218184204.png]]
Podemos probar con otro dominio, como udemy, y vemos que nos encuentra un correo:
![[Pasted image 20231218184343.png]]
