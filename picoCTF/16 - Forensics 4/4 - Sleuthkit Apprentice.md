
## DESCRIPCIÓN
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/138/disk.flag.img.gz)
## SOLUCIÓN
Nos vamos a la carpeta de /tmp, ahi descargamos la imagen y la descomprimimos con gzip -d, una vez descomprimida le damos a:

```
mmls disk.flag.img
```

y nos devuelve varios numeros, vamos probando de uno en uno de start con fls, hasta que con el tercero:

```
fls -o 360448 disk.flag.img 
```

Hasta que observamos que el d/d 1995 es el root, nos vamos a el:

```
fls -o 360448 disk.flag.img 1995
```

luego a my_forder:

```
fls -o 360448 disk.flag.img 3981
```

y ahi hay un txt que es la flag, el r/r 2371, lo abrimos con icat:

```
icat -o 360448 disk.flag.img 2371
```

y obtenemos la flag:

picoCTF{by73_5urf3r_2f22df38}

## NOTAS ADICIONALES

## REFERENCIAS




