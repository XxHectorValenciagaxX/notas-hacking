
## DESCRIPCIÓN
This is a really weird text file.

Can you find the flag?Get the flag from [TXT](https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt).
## SOLUCIÓN
Descargamos la imagen con wget y con el siguiente comando:

```
xxd -l 20 flag.txt 
```

Se puede observar que a pesar de ser un archivo .txt, este esta identificado como un png (las primeras letras son las que lo identifican, estos son los magic bites), por lo tanto la convertimos a png con:

```
mv flag.txt flag.png
```

al abrir la imagen:

```
open flag.png
```

y obtenemos la flag:

picoCTF{now_you_know_about_extensions}
## NOTAS ADICIONALES
- La flag que se encuentra en la imagen se tiene que copiar manualmente, pero IAs si pueden substraer el texto.
## REFERENCIAS





