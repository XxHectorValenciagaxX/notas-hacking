
## DESCRIPCIÓN
Can you login to this website?

Try to login [here](http://saturn.picoctf.net:52941/).
## SOLUCIÓN
Al intentar inician secion nos aparece que primero revisa si el username concuerda con admin y despues checa la contraseña, a sabiendas de esto hacemos inyeccion de sql.

Colocamos admin en el username

y en la contraseña colocamos:

```
' or 1=1;
```
Ingresamos correctamente y la flag se encuentra en el codigo fuente:

y obtenemos la flag:

picoCTF{L00k5_l1k3_y0u_solv3d_it_ec8a64c7}
## NOTAS ADICIONALES

## REFERENCIAS





