
## DESCRIPCIÓN
How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 59547
Username: picoplayer 
Password: bLgSMmbY6X
```
## SOLUCIÓN
Nos conectamos al servidor y comenzamos observando que el usuario no cuenta con permisos sudo, lo de "como se automatizan las tareas" de la descripcion del reto nos da una pista hacia cron, hay que leer las configuraciones generales del sistema, para ello nos vamos a la carpeta etc y generalmente se encuentran en la carpeta "crontab":

```
cd /etc
cat crontab
```

y encontramos la flag:

picoCTF{Sch3DUL7NG_T45K3_L1NUX_1b4d8744}
## NOTAS ADICIONALES
- Tambien se puede encontrar con:
```
grep -r picoCTF .
```

## REFERENCIAS



