
## DESCRIPCIÓN
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?

Additional details will be available after launching your challenge instance.

Connect to fickle-tempest.picoctf.net 55577.

## SOLUCIÓN
Al darle al launch instance, se activa el host de fickle-tempest.picoctf.net, con la ayuda del net cat, nos conectamos al puerto 55577, y guardamos el output en un archivo .txt con el siguiente comando:

```
nc fickle-tempest.picoctf.net 55577 > flag.txt
```

Despues con la ayuda de grep encontramos la flag entre toda la cadena de texto:

```
grep CTF flag.txt
```
 
 y encontramos la flag:

picoCTF{digital_plumb3r_00da27CC}
## NOTAS ADICIONALES
Otra solución es:

```
nc fickle-tempest.picoctf.net 55577 | grep CTF
```

## REFERENCIAS

