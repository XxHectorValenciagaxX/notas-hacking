
## DESCRIPCIÓN
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Access checker program: `nc saturn.picoctf.net 56741`
## SOLUCIÓN
Nos ubicamos en la carpete de tmp, con cd /tmp, despues descargamos ahi la imagen del disco, la descomprimimos con gzip -d y ahi dentro ponemos:

```
mmls disk.img
```

Obtenemos los numeros de la ultima cadena de length de Linux, que es 202752, utilizamos el comando de net cat que nos dieron y cuando nos pregunte el lenght le ponemos eso:

```
nc saturn.picoctf.net 56741

202752
```

y obtenemos la flag:

picoCTF{mm15_f7w!}

## NOTAS ADICIONALES

## REFERENCIAS




