
## DESCRIPCIÓN
Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.

Our flag printing service has started glitching!

`$ nc saturn.picoctf.net 57436`
## SOLUCIÓN
Al darle al launch instance, se activa el host de saturn.picoctf.net en el puerto 57436, nos conectamos con net cat

```
nc saturn.picoctf.net 57436
```

Y obtenemos la flag incompleta, ya que esta en hexadecimal y además se debe a transformar a su respectivo caracter ASCII (eso hace la función chr):

'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'

Tan solo nos vamos a la terminal, ingresamos a python y colocamos el comando:

```
print('picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}')
```
 
 y encontramos la flag:

picoCTF{gl17ch_m3_n07_9c42a45d}

## NOTAS ADICIONALES

## REFERENCIAS

