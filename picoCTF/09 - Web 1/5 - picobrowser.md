
## DESCRIPCIÓN
his website can be rendered only by picobrowser, go and catch the flag!

http://fickle-tempest.picoctf.net:62992
## SOLUCIÓN
Ingresamos al http desde el navegador de firefox, la pista que nos indican es que solo se puede acceder desde el navegador de picobrowser, para ello obsermavos el html de flag en la seccion de Network y se puede observar que la respuesta de la conexion se encuentra desde User-Agent, el cual tiene el valor de Mozilla Firefox, para cambiarlo copiamos la url y lo modificamos con curl:

```
curl 'http://fickle-tempest.picoctf.net:62992/flag'   -H 'User-Agent: picobrowser' | grep pico
```

Y obtenemos la flag:

picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}
## NOTAS ADICIONALES

## REFERENCIAS




