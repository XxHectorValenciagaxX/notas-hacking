
## DESCRIPCIÓN
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image.

[dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/27cbd6a2ed4a59d600f2a24c1ccaa6de66f9aeee95d6b365160fd75649e45f1b/dds1-alpine.flag.img.gz)
## SOLUCIÓN
Descargamos el archivo y lo descomprimimos con gzip -d, una vez descomprimido lo leemos con strings:

```
strings dds1-alpine.flag.img | grep picoCTF
```

y obtenemos la flag:

picoCTF{f0r3ns1c4t0r_n30phyt3_5e56e786}

## NOTAS ADICIONALES

## REFERENCIAS




