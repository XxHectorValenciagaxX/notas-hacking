
## DESCRIPCIÓN
Help us test the form by submiting the username as `test` and password as `test!`The website running [here](http://saturn.picoctf.net:62976/).
## SOLUCIÓN
Entrar a la página, después interceptar el redireccionamiento y con ello conseguir nuestra flag

- Primero entramos al link que se nos da, después abrimos burpsuite y tratamos de loguearnos, interceptando, luego vamos avanzando poco a poco y los ids, los pasamos a decodificar en base64 en cyberchef

y obtenemos la flag:

picoCTF{proxies_all_the_way_d1c0b112}

## NOTAS ADICIONALES

## REFERENCIAS
- https://www.base64decode.org/



