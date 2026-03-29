
## DESCRIPCIÓN
Files can always be changed in a secret way. Can you find the flag?[cat.jpg](https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg)
## SOLUCIÓN
Descargamos la imagen y vemos los metadatos con:

```
exiftool cat.jpg
```

ahi en license vemos un codigo en base64, lo decodificamos. 

y obtenemos la flag:

picoCTF{the_m3tadata_1s_modified}

## NOTAS ADICIONALES

## REFERENCIAS




