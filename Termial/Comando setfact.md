#Terminal #PinguinoMario #HackingEtico 
El comando `setfacl` se utiliza para establecer listas de control de acceso (ACL). Las ACL permiten un control más detallado sobre los permisos de acceso a archivos y directorios en comparación con los permisos tradicionales de Unix.

`setfacl` se utiliza para gestionar las Listas de Control de Acceso (ACL), que permiten definir permisos más detallados que los proporcionados por `chmod`.

--------------------

**Ver ACL existentes:** Puedes usar el comando `getfacl` para ver las ACL existentes en un archivo o directorio. Por ejemplo:
```bash
getfacl carpeta1
```
![[Pasted image 20231212152636.png]]
**Establecer nuevas ACL:**
Para establecer una nueva ACL, puedes usar `setfacl`. De tal forma que podemos asignar permisos a una carpeta para un usuario en específico. Por ejemplo, vamos a crear una carpeta donde nadie tenga ningún permiso:
![[Pasted image 20231212153035.png]]
Y ahora con setfacl le damos permisos sólo al usuario Esteban:
```bash
setfacl -m u:esteban:rwx carpeta
```
![[Pasted image 20231212153119.png]]
Nos logueamos como el usuario Esteban y vamos a ver que con este usuario sí tenemos permisos de rwx sobre esta carpeta:
![[Pasted image 20231212154033.png]]
Sin embargo, si ahora somos otro usuario, por ejemplo mario, veremos que no tenemos permisos:
![[Pasted image 20231212153238.png]]
**Crear ACL a grupos**
También puedes establecer ACL para grupos:
```bash
setfacl -m g:grupo12:rw carpeta1
```
**Eliminar una ACL**
Esto eliminará la entrada de ACL para el usuario especificado:
```bash
setfacl -x u:usuario nombre_del_archivo
```