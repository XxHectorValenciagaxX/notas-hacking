
## DESCRIPCIÓN
A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?Access the server using `nc verbal-sleep.picoctf.net 52885`
## SOLUCIÓN
Utilizamos netcat para ingresar a la pagina que se nos indica, después, vamos obteniedo los hashes y simplemente los vamos mandando a la página para que nos de las contraseñas.

y obtenemos la flag:

picoCTF{UseStr0nG_h@shEs_&PaSswDs!_5b836723}

## NOTAS ADICIONALES

## REFERENCIAS
- https://crackstation.net/




