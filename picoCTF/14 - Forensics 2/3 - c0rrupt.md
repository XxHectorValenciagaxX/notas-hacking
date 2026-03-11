
## DESCRIPCIÓN
We found this [file](https://challenge-files.picoctf.net/c_fickle_tempest/87bdc8ce30b177d033b3d68bca4647950bb07304032861baa912ebe08701d355/mystery). Recover the flag.
## SOLUCIÓN
Descargamos el archivo llamado mystery y lo revisamos con:

```
xxd -g 1 -l 100 mystery 
```

Y observamos que para ser un PNG, la cabecera esta corrupta, debería ser 89 50 4E 47 0D 0A 1A 0A, entonces los modificamos con hexeditor, luego revisamos con pngcheck y vemos que el chunk de IHDR esta corrupto, igual - corregir IHDR : 43 22 44 52 por 49 48 44 52.

Luego - corregimos `pHys`, cambiamos `aa 00 16 25 00 00 16 25` por `00 00 16 25 00 00 16 25` 

Después corregimos el tamaño del chunk, cambiamos `AA AA FF A5` por `00 00 FF A5` y también corregir chunk anterior para que diga `IDAT` , cambiamos `AB 44 45 54` por `49 44 41 54`.

Abrimos el archivo con open.

y obtenemos la flag:

picoCTF{c0rrupt10n_1847995}
## NOTAS ADICIONALES

## REFERENCIAS
- https://stylesuxx.github.io/steganography/




