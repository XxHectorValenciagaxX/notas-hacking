
## DESCRIPCIÓN
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
## SOLUCIÓN
Primero descargamos el archivo de python:

```
wget https://artifacts.picoctf.net/c/11/level1.py

wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
```

El descargar los archivos obtenemos un ejecutable de python y otro un .txt que es el crack, cada uno debe de estar en la misma carpeta, el crack es necesario para correr el programa, mas no tiene la contraseña, al ver el codigo de python con:

```
cat level1.py
```

en la linea de codigo:

if( user_pw == "1e1a"):

esa es la contraseña, corremos el programa con:

```
python level1.py
```

Ingresamos 1e1a y obtenemos la flag:

picoCTF{545h_r1ng1ng_fa343060}
## NOTAS ADICIONALES

## REFERENCIAS



