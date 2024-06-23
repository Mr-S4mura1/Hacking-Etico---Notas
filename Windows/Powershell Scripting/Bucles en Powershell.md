#Powershell #WIndows #PinguinoMario #HackingEtico 
### BUCLE FOR
```powershell
$frutas = "Manzana", "Banana", "Naranja", "Pera", "Melón"

for ($i = 0; $i -lt $frutas.Count; $i++) {
    Write-Host $frutas[$i]
}
```
![[Pasted image 20230509150805.png]]
También podríamos recorrer todos los elementos de un documento de texto, de la siguiente forma:
```powershell
$archivo = Get-Content "direcciones_ip.txt"

for ($i = 0; $i -lt $archivo.Count; $i++) {
    Write-Host $archivo[$i]
}
```