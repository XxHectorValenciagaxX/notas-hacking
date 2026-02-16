
## DESCRIPCIÓN
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## SOLUCIÓN
Primero descargamos el archivo de python:

```
wget https://artifacts.picoctf.net/c/26/fixme1.py
```

El archivo de python cuenta con un error, el print que imprime la bandera esta mal identado, con la ayuda de nano lo corregimos:

```
nano fixme1.py
```

de:
...
	print(...)

a:

...
print(...)

Al ejecutarlo con:

```
python fixme1.py
```

Obtenemos la flag:

picoCTF{1nd3nt1ty_cr1515_09ee727a}
## NOTAS ADICIONALES

## REFERENCIAS



