
## DESCRIPCIÓN
Find the flag in this [picture](https://challenge-files.picoctf.net/c_fickle_tempest/d534c920bd33d42b413e67d21cacbf7aa232c4823ce29872eca285471558f00a/pico_img.png).
## SOLUCIÓN
Descargamos la imagen con wget y vemos los metadatos con exiftool:

```
exiftool pico_img.png  
```

Y al revisar los metadatos observamos que en el Artist se encuentra la flag.

y obtenemos la flag:

picoCTF{s0_m3ta_74af23ab}
## NOTAS ADICIONALES
- Existen otras formas de hacerlo menos manuales:

```
strings pico_img.png | grep picoCTF
```

```
grep -a picoCTF pico_img.png
```
## REFERENCIAS





