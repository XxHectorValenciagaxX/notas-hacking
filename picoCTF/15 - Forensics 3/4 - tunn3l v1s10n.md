
## DESCRIPCIÓN
We found this file. Recover the flag.[tunn3l_v1s10n](https://challenge-files.picoctf.net/c_wily_courier/626df9feed926c1e1280804f5d87fde5576e266ff250a819a5528b0471b0f3f7/tunn3l_v1s10n)
## SOLUCIÓN
Descargamos la imagen y con la herramienta exiftool observamos sus metadatos, y podemos ver que es un tipo de archivo BMP, buscamos en internet el formato BMP e intentamos corregirla con hexeditor:

En el primer renglon cambiamos:

```
 42 4D 8E 26  2C 00 00 00   00 00 BA D0  00 00 BA D0
```

Por:

```
42 4D 8E 26  2C 00 00 00   00 00 28 00  00 00 28 00
```

Y con eso esta arreglada, sin embargo al abrirla aparece no flag, si vemos otra vez con exiftool vemos que la imagen es mas ancha que alta, por lo que igual modificamos en el segundo renglon:

```
00 00 6E 04  00 00 32 01   00 00 01 00  18 00 00 00
```

El 6E 04 (esta al reves) es el alto en hexadecimal, entonces le ponemos lo mismo en el ancho:

```
00 00 6E 04  00 00 6E 04   00 00 01 00  18 00 00 00
```

Y al abrir la imagen con open.

y obtenemos la flag:

picoCTF{qu1t3_a_v13w_2020}
## NOTAS ADICIONALES

## REFERENCIAS




