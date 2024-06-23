#Terminal #PinguinoMario #HackingEtico 
El comando `umask` se utiliza para establecer los permisos predeterminados para los nuevos archivos y directorios creados por un usuario. El nombre "umask" proviene de "user mask" o "user file creation mask". La máscara umask se utiliza para ocultar (o restar) ciertos permisos de los permisos predeterminados que se asignarían a un archivo o directorio recién creado.

La máscara umask es un valor de tres dígitos octales (0-7) que se aplica al inverso de los permisos que se desean ocultar. Cada dígito en la máscara representa un conjunto específico de permisos (lectura, escritura y ejecución) para el propietario, el grupo y otros. La máscara umask se resta de los permisos predeterminados para determinar los permisos finales.

La estructura de la máscara umask es la siguiente:

```bash
umask [dígito de usuario] [dígito de grupo] [dígito de otros]
```

- **Dígito de usuario:** Representa los permisos del propietario.
- **Dígito de grupo:** Representa los permisos del grupo.
- **Dígito de otros:** Representa los permisos para otros usuarios.

Ejemplos de máscaras umask comunes:

- `umask 022`: Esto significa que se quitará la escritura para el grupo y otros. Los nuevos archivos tendrán permisos 644 (rw-r--r--).
- `umask 077`: Esto significa que se quitarán todos los permisos para grupo y otros. Los nuevos archivos tendrán permisos 600 (rw-------).
- `umask 002`: Esto significa que se quitará la escritura para otros. Los nuevos archivos tendrán permisos 664 (rw-rw-r--).