#Terminal #HackingEtico 
Con este comando podremos tener un shell interactiva, mucho mejor de la que obtemos al estar por escucha. Este comando va a permitir esa shell interactive.

```bash
script /dev/null -c bash
python -c ‘import pty;pty.spawn(“/bin/bash”)’
```

