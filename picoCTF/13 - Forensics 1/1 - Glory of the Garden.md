
## DESCRIPCIÓN
This file contains more than it seems.

Get the flag from [garden.jpg](https://challenge-files.picoctf.net/c_fickle_tempest/150b6eaad43200d3dc91f98c390e4c6168620b57d0b95a7e9d04c92910bbbe16/garden.jpg).
## SOLUCIÓN
Descargamos la imagen con wget y vemos el contenido de la imagen con el hexeditor:

```
xxd garden.jpg
```

Y al final de toda la cadena binaria se encuentra la flag.

y obtenemos la flag:

picoCTF{more_than_m33ts_the_3y3a63b5b27}
## NOTAS ADICIONALES
- Existen otras formas de hacerlo menos manuales:

```
strings garden.jpg | grep picoCTF
```

```
grep -a picoCTF garden.jpg
```
## REFERENCIAS





