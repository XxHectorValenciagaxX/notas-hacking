
## DESCRIPCIÓN
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?Image: [dolls.jpg](https://challenge-files.picoctf.net/c_wily_courier/f1f4181c217358672b720e801df28731166311181fd73b364baa4479f8500044/dolls.jpg)

## SOLUCIÓN
Descargamos la imagen y con la herramienta binwalk (utilizada para examinar firmware, como modems):

```
binwalk dolls.jpg
```

y observamos:
```
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378933, uncompressed size: 383920, name: base_images/2_c.jpg
651591        0x9F147         End of Zip archive, footer length: 22
```

Esto nos indica que adentro se encuentra un zip con una imagen dentro de la imagen, entonces:

```
unzip dolls.jpg
```

Nos crea una carpeta base_images, dentro esta una imagen con una doll mas pequeña, repetimos el proceso 4 veces hasta obtener un flag.txt.

y obtenemos la flag:

picoCTF{LL9lb1dR4QbGe4l4iWCvGq9pdtwt7392}
## NOTAS ADICIONALES

## REFERENCIAS




