#Powershell #WIndows #PinguinoMario #HackingEtico 
Funcionan igual que en bash, por ejemplo ordenando los procesos del sistema por orden alfabético:
![[Pasted image 20221217104150.png]]
Por ejemplo, si quiero visualizar el contenido de un archivo y aplicar una tubería para que me busque algo, lo haría de esta forma:
```powershell
Get-Content direcciones_ip.txt | Select-String -Pattern "192"
```
![[Pasted image 20230509151233.png]]