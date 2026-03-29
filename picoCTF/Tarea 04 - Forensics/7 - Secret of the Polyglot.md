
## DESCRIPCIÓN
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/7/flag2of2-final.pdf).
## SOLUCIÓN
Descargamos el archivo pdf, al abrirlo vemos que solo tiene la segunda parte de la flag, al ver los bytes con hexeditor vemos que en realidad esta creado como un png, por lo que lo convertimos:

```
convert flag2of2-final.pdf flag2of2-final.png
```

Al abrirlo esta la primera parte de la flag.

y obtenemos la flag:

picoCTF{f1u3n7_1n_pn9_&_pdf_53b741d6}

## NOTAS ADICIONALES

## REFERENCIAS




