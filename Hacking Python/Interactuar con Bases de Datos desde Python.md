#HackingPython #PinguinoMario #HackingEtico
Lo primero será instalar esta librería de Python para gestionar bases de datos MySQL desde Python:
![[Pasted image 20221217093730.png]]
Y lo primero será establecer la conexión:
![[Pasted image 20221217093748.png]]
![[Pasted image 20221217093755.png]]
Ahora vamos a hacer una consulta:
```python
import mysql.connector

connection = mysql.connector.connect(user='root', password='123123',
                                    host='localhost',
                                    database='hr',
                                    port='3306',)

print(connection)

cursor = connection.cursor()
cursor.execute("SELECT first_name FROM employees")

consulta = cursor.fetchall()
print(consulta)
```
![[Pasted image 20221217093818.png]]
Ahora vamos a procesar esta consulta para volcarla dentro de un documento de texto:
![[Pasted image 20221217093834.png]]
![[Pasted image 20221217093839.png]]
