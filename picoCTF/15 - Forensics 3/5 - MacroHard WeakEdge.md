
## DESCRIPCIÓN
I've hidden a flag in this file. Can you find it?[Forensics_is_fun.pptm](https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm)
## SOLUCIÓN
Descargamos el archivo .pptm que es de diapositivas, y segun eso la flag se encuentra en las macros, pero al ir no esta.

Entonces descomprimimos el archivo con unzip y hasta el final vemos que hay una carpeta llamada hidden, vemos su contenido con cat y vemos que tiene una serie de letras, en realidad es una codificacion en base64 y tenemos que quitarle los espacios, podemos hacer todo esto con:

```
cat ppt/slideMasters/hidden | tr -d ' ' | base64 -d             
```

y obtenemos la flag:

picoCTF{D1d_u_kn0w_ppts_r_z1p5}
## NOTAS ADICIONALES

## REFERENCIAS




