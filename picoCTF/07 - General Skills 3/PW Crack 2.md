
## DESCRIPCIÓN
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## SOLUCIÓN
Primero descargamos el archivo de python:

```
wget https://artifacts.picoctf.net/c/14/level2.py

wget https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
```

El descargar los archivos obtenemos un ejecutable de python y otro un .txt que es el crack, cada uno debe de estar en la misma carpeta, el crack es necesario para correr el programa, mas no tiene la contraseña, al ver el codigo de python con:

```
cat level2.py
```

en la linea de codigo:

if( user_pw == "chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)"):

Se encuentra la contraseña encriptada, con ayuda de python la desencriptamos:}

```
python

print(chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39))
```

4ec9

esa es la contraseña, corremos el programa con:

```
python level2.py
```

Ingresamos 1e1a y obtenemos la flag:

picoCTF{tr45h_51ng1ng_9701e681}
## NOTAS ADICIONALES
- Es prácticamente lo mismo, pero podemos modificar el código de level2.py y ahí mismo colocamos un print para que nos devuelva la flag en la misma ejecución, pero es lo mismo de todos modos.
## REFERENCIAS



