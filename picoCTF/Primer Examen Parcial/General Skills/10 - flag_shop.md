
## DESCRIPCIÓN
There's a flag shop selling stuff, can you buy a flag?[Source](https://challenge-files.picoctf.net/c_fickle_tempest/8ff1a012a01d1cbdaff34d98276201480b3a664509284c48bb108e0e01d3551d/store.c). Connect with nc fickle-tempest.picoctf.net 49241.

## SOLUCIÓN
Entrar a la página y causar un integer overflow para poder comprar la flag

- Primero entramos a la página, después compramos banderas, pero una cantidad "2400000" para con esto causar que nuestro estado de cuenta gane dinero por el overflow y con ello comprar nuestra flag

y obtenemos la flag:

picoCTF{m0n3y_bag5_4E85dfe5}

## NOTAS ADICIONALES

## REFERENCIAS




