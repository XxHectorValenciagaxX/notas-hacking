
## DESCRIPCIÓN
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

## SOLUCIÓN
Primero descargamos el file (warm) con el comando:

```
wget https://challenge-files.picoctf.net/c_wily_courier/89a0e56b3f2697fe5d597b2805202b86693dcb0e04aec062e11fe66edbbd04aa/warm
```

Una vez obtenemos el archivo, al ser un archivo binario, lo procesamos con strings y buscamos la flag:

```
strings warm | grep pico
```

y obtenemos la flag:

picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
## NOTAS ADICIONALES
- La solución pensada para este problema es hacer el archivo ejecutable, ejecutarlo, y utilizar el comando -h o --help para que nos devuelva la flag:

 Una vez descargado el archivo:
 
```
chmod +x warm | ./warm -h
```

y obtenemos la flag.
## REFERENCIAS



