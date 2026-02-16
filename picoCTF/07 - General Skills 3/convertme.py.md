
## DESCRIPCIÓN
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/22/convertme.py)
## SOLUCIÓN
Primero descargamos el archivo de python:

```
wget https://artifacts.picoctf.net/c/22/convertme.py
```

Al ejecutarlo con:

```
python convertme.py
```

Nos pregunta cuanto es 13 en decimal a base 2 (binaria), al utilizar una página web de conversión ingresamos la respuesta de: 1101 y nos da la flag:

picoCTF{4ll_y0ur_b4535_762f748e}
## NOTAS ADICIONALES
- El wget -q es el comando --quiet, que sirve para que no muestre la info mientras se descarga un archivo.
## REFERENCIAS
- https://wims.univ-cotedazur.fr/wims/wims.cgi?session=UC7E366010.1&lang=es&cmd=reply&module=tool%2Fnumber%2Fbaseconv.es&input=13&ibase=10&obase=2&prec=30


