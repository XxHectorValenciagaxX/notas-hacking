
## DESCRIPCIÓN
Can you get the flag?

Go to this [website](http://saturn.picoctf.net:49562/) and see what you can discover.
## SOLUCIÓN
Entramos a la pagina al intenar loguear como guest no sirve, por lo que ingresamos al gues.js y vemos que el valor de document.cookie = 'isAdmin = 0', con ayuda de burpsuite interceptamos la peticion y cambiamos el valor por 1, entonces entramos.

y obtenemos la flag:

picoCTF{gr4d3_A_c00k13_0d351e23}
## NOTAS ADICIONALES

## REFERENCIAS





