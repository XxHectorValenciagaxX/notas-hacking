
## DESCRIPCIÓN
Find the flag being held on this server to get ahead of the competition

http://wily-courier.picoctf.net:60546/
## SOLUCIÓN
Ingresamos al http desde el navegador de firefox, y observamos dos botones, uno cambia la pantalla a rojo y el otro al azul, hay que entender que para recibir peticiones hay varias formas, con GET (usado en el rojo), con POST (usado en el azul), si colocamos:

```
curl -X GET http://wily-courier.picoctf.net:60546/index.php

curl -X POST http://wily-courier.picoctf.net:60546/index.php
```

Podemos observar el codigo que hace el cambio de color de la pagina, sin embargo hay una tercera forma, la pista nos dice que tambien existe HEAD, si lo colocamos (ejecutandolo con -I):
```
curl -I http://wily-courier.picoctf.net:60546/index.php
```

Y obtenemos la flag:

picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
## NOTAS ADICIONALES

## REFERENCIAS





