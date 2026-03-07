
## DESCRIPCIÓN
We have several pages hidden. Can you find the one with the flag?

The website is running [here](http://saturn.picoctf.net:62599/).
## SOLUCIÓN
Entramos al codigo fuente y vemos que la imagen que se muestra se encuentra en una carpeta llamada secret, nos vamos ahi y nos devuelve un gif, observamos que hay un archivo .css oculto en una carpeta llamada hidden, tambien entramos ahi y nos devuelve un login, que esta almacenado en una carpeta llamada superhidden, ahi dice que lo encontramos, la flag se encuentra en el codigo fuente:

http://saturn.picoctf.net:58764/secret/hidden/superhidden/

y obtenemos la flag:

picoCTF{succ3ss_@h3n1c@10n_790d2615}
## NOTAS ADICIONALES

## REFERENCIAS





