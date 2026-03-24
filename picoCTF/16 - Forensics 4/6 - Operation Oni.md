
## DESCRIPCIÓN
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://artifacts.picoctf.net/c/69/disk.img.gz)
- Remote machine: `ssh -i key_file -p 62307 ctf-player@saturn.picoctf.net`

## SOLUCIÓN
Descargamos el archivo en tmp, lo descomprimimos, con mmls vemos los datos de start, y con fls nos vamos a root y vemos un archivo .ssh, nos metemos:

```
fls -o 206848 disk.img 3916
```

y en 2345 vemos una llave, la obtenemos con icat:

```
icat -o 206848 disk.img 2345 > id_ed25519
```

la ejecutamos con:

```
chmod 600 id_ed25519
```

una vez ejecutado ejecutamos el comando del ssh del pico con esa misma llave:

```
ssh -i id_ed25519 -p 62307 ctf-player@saturn.picoctf.net
```

le damos a yes, ingresamos al server y al darle ls vemos la flag.txt la abrimos con cat.

y obtenemos la flag:

picoCTF{k3y_5l3u7h_339601ed}

## NOTAS ADICIONALES

## REFERENCIAS




