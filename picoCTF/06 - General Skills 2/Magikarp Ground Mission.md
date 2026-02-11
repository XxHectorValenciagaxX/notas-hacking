
## DESCRIPCIÓN
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.

Additional details will be available after launching your challenge instance.

Login via `ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `51197`.
## SOLUCIÓN
Nos conectamos al servidor:

```
picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}
```

Una vez ahí con ls encontramos un archivo llamado 1of3.flag.txt que al abrirlo con cat obtenemos el primer pedazo de la flag:

picoCTF{xxsh_

el segundo archivo de instrucciones para el segundo pedazo dice que nos vallamos a la raíz con el comando:

```
cd /
```

Ahí encontramos el segundo pedazo:

0ut_0f_//4t3r

y las instrucciones del tercer pedazo que dice que nos vallamos al home con:

```
cd ~
```

encontramos el tercer pedazo:

0b24fc4f}

Al final se solo los juntamos y obtenemos la flag:

picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}
## NOTAS ADICIONALES
-  cd /  es para ir a la raiz del entorno.
-  cd ~ es para ir al home
-  ls -la es para encontrar (con detalles) archivos ocultos.
## REFERENCIAS



