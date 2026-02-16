
## DESCRIPCIÓN
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## SOLUCIÓN
Primero descargamos el archivo de python:

```
wget https://artifacts.picoctf.net/c/16/level3.py

wget https://artifacts.picoctf.net/c/16/level3.flag.txt.enc

wget https://artifacts.picoctf.net/c/16/level3.hash.bin
```

Descargamos los archivos en el mismo directorio, el achivo de python cuenta con 7 posibles contraseñas, tambíen tenemos un archivo hash el cuál contiene encriptada la contraseña, 

```
cat level2.py
```

Ingresamos de una en una y descubrimos que la ultima es la correcta:

865e

y entonces obtenemos la flag:

picoCTF{m45h_fl1ng1ng_2b072a90}
## NOTAS ADICIONALES
- Para no buscar de una en una podemos colocar un ciclo for con la lista de contraseñas para que el programa las pruebe automáticamente, y la que coincida con el hash esa sera la correcta.
## REFERENCIAS



