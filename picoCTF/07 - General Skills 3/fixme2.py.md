
## DESCRIPCIÓN
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## SOLUCIÓN
Primero descargamos el archivo de python:

```
wget https://artifacts.picoctf.net/c/6/fixme2.py
```

El archivo de python cuenta con un error, el if que revisa el estado de la flag esta asignando un valor en vez de compararlo, lo corregimos:

```
nano fixme1.py
```

de:

if flag = "":

a:

if flag == "":

Al ejecutarlo con:

```
python fixme2.py
```

Obtenemos la flag:

picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
## NOTAS ADICIONALES

## REFERENCIAS



