
## DESCRIPCIÓN
Can you abuse the banner?The server has been leaking some crucial information on `tethys.picoctf.net 64306`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 59072`. From the above information abuse the machine and find the flag in the /root directory.
## SOLUCIÓN
Entrar a la página y hacer un link simbólico para conseguir la flag

- Primero es entrar a la pagina de apoyo que tiene la contraseña y llevárnosla, luego a la página del reto y allí contestamos las 3 preguntas que nos hace, después borramos el banner "rm banner" y luego hacemos un link simbólico "ln -s /root/flag.txt ./banner" entre la flag y el banner para que la próxima vez que nos conectemos directamente nos abra la flag y con ello al volver a conectarnos, tenemos la flag

y obtenemos la flag:

picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_8126c9b0}

## NOTAS ADICIONALES

## REFERENCIAS
- 



