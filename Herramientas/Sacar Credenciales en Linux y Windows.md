Para sacar todas las credenciales de  un sistema operativo vamos a clonar el siguiente repositorio en Linux o Windows, dependiendo donde queramos sacar dichas credenciales.

```bash 
git clone https://github.com/AlessandroZ/LaZagne.git
```

![[Pasted image 20240115124113.png]]

Despues de clonar dicho repositorio vamos a instalar los requerimientos necesarios para este repo, por lo que vamos a instalarlos con el siguiente comando.

```bash 
cd LaZagne
pip install -r requirements.txt
cd Linux
```

Despues de haber entrado a la carpeta de linux y ejecutar el .py que hay allí y colocar al lado el parámetro all ya tendremos todas nuestra credenciales.

![[Pasted image 20240115124517.png]]


Para sacar credenciales de Windows usaremos esta misma herramienta o la herramienta de *mimikatz*, en el siguiente repositorio podrás decargarlo. https://github.com/ParrotSec/mimikatz.git  y para utilizarlo solo falta ejecutarlo y colocar el siguiente comando.

```bash 
sekurlsa::logonpasswords
```


