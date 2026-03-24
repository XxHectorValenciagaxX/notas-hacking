
## DESCRIPCIÓN
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/214/disk.flag.img.gz)
## SOLUCIÓN
Descargamos la imagen en tmp, la descomprimimos y con mmls obtenemos el ultimo numero de start, y con fls lo vemos, nos vamos hasta root y vemos la flag que esta codificada en .enc:

```
fls -o 411648 disk.flag.img 472 
```

la cual es la 1782, la vemos con icat pero esta encryptada, la guardamos:

```
icat -o 411648 disk.flag.img 1782 > flag.txt.enc 
```

con strings vemos la forma de desencryptarla:

```
strings disk.flag.img | grep flag.txt 
```

anadimos el -d al comando, que la entrada sea el flag.txt.enc y la salida el flag.txt:

```
openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
```

leemos el flag.txt generado.

y obtenemos la flag:

picoCTF{h4un71ng_p457_1d02081e}
## NOTAS ADICIONALES

## REFERENCIAS




