
## DESCRIPCIÓN
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/262/flag.png).
## SOLUCIÓN
Descargamos la imagen y con binwalk observamos que contiene una carpeta secret/flag.png adentro, la descomprimimos:

```
binwalk -e flag.png
```

ingresamos a ___flag.png.extracted/secret/flag.png

Abrimos la imagen y copiamos la flag letra por letra.

y obtenemos la flag:

picoCTF{Hiddinng_An_imag3_within_@n_ima9e_82101824}

## NOTAS ADICIONALES

## REFERENCIAS




