
## DESCRIPCIÓN
There's an interesting script in the user's home directory

Additional details will be available after launching your challenge instance.

The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

```
Hostname: saturn.picoctf.net
Port:     50029
Username: picoplayer
Password: password
```


## SOLUCIÓN
Como nos tenemos que conectar a un servidor ssh y contamos tanto con el username, port y host, nos conectamos con el comando:

```
ssh -p 50029 picoplayer@saturn.picoctf.net
```

Después ingresamos con yes, e ingresamos la contraseña. Una vez adentro, colocamos ls y encontramos un ejecutable llamado useless, al revisar su estructura con cat dice que revisemos el manual, para ello utilizamos el comando:

```
man useless
```

Al final se encuentra la flag:

picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_6140}
## NOTAS ADICIONALES
-  Comando man, es el manual, es una ayuda integrada en Linux, sirve para mostrar las paginas de documentación de los comandos, programas, bibliotecas y archivos de configuración instalados en el sistema.

## REFERENCIAS
- https://gemini.google.com


