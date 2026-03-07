
## DESCRIPCIÓN
The flag is somewhere on this web application not necessarily on the website.

Find it.Check [this](http://saturn.picoctf.net:56781/) out.
## SOLUCIÓN
Nos vamos al archivo robots.txt y vemos una codificacion en base64, lo traducimos y nos dice: 

1. **`ZmxhZzEudHh0`** decodifica a: **`flag1.txt`**

2. **`anMvbXlmaWxlLnR4dA==`** decodifica a: **`js/myfile.txt`**

intenamos con la primera opcion sin exito, pero con la segunda nos vamos a:

http://saturn.picoctf.net:56781/js/myfile.txt

y obtenemos la flag:

picoCTF{Who_D03sN7_L1k5_90B0T5_032f1c2b}
## NOTAS ADICIONALES

## REFERENCIAS





