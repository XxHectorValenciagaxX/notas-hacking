
## DESCRIPCIÓN
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.picoctf.net/c_fickle_tempest/4de4b105d28cb6df34d9805217f2460b978a37dafc3dfc50edadd8d424dd311a/whitepages.txt) is all blank!
## SOLUCIÓN
Descargamos el archivo llamado y lo revisamos con:

```
xxd -g 1 -l 100 whitepages.txt 
```

Visualizamos el hexdump del archivo y vemos que es una seuencia de caracteres unicode (e2 80 83 y 20 )

Y reemplazamos e2 80 83 por 0s y 20 por 1s

`sed 's/\xe2\x80\x83/0/g' whitepages.txt | sed 's/\x20/1/g'`

Nos devuelve un texto en binario, solo lo traducimos.

y obtenemos la flag:

picoCTF{not_all_spaces_are_created_equal_f5d46aff52c6e17f9fd6317b33d2d783}

## NOTAS ADICIONALES

## REFERENCIAS
- https://stylesuxx.github.io/steganography/




