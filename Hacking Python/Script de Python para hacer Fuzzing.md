#HackingPython #PinguinoMario #HackingEtico
Podemos hacer fuzzing con python usando el siguiente código:
```python
import argparse
import requests
from tqdm import tqdm

parser = argparse.ArgumentParser(description="Script de fuzzing de directorios web")
parser.add_argument("url", help="URL base para el fuzzing")
parser.add_argument("diccionario", help="Archivo de diccionario")
args = parser.parse_args()

with open(args.diccionario) as file:
    wordlist = file.read().splitlines()

try:
    barrita = tqdm(total=len(wordlist), desc="Progreso", unit="urls", dynamic_ncols=True)

    for linea in wordlist:
        url_completa = args.url + linea  # Corregido para usar args.url en lugar de url

        response = requests.get(url_completa)

        if response.status_code == 200:
            tqdm.write(f"Directorio encontrado: {url_completa}")

        barrita.update(1)

except KeyboardInterrupt:
    print("\nScript interrumpido por el usuario (Ctrl + C).")
finally:
    barrita.close()
```
![[Pasted image 20230917121721.png]]
