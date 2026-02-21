
## DESCRIPCIÓN
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/77/challenge.zip)

## SOLUCIÓN
Una vez descomprimido el archivo, nos ubicamos en la carpeta y encontramos los archivos ocultos con:

```
ls -a
```

obsrervamos que tiene un control de versiones con git, vemos las versiones anteriroes del message.txt:

```
git log
```

y podemos ver la version en la que se encontraba la flag:

```
git show 3d5ec8a26ee7b092a1760fea18f384c35e435139
```

y encontramos la flag:

picoCTF{s@n1t1z3_30e86d36}
## NOTAS ADICIONALES

## REFERENCIAS



