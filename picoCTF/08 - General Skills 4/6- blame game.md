
## DESCRIPCIÓN
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/73/challenge.zip)
## SOLUCIÓN
Una vez descomprimido el archivo, nos ubicamos en la carpeta y encontramos los archivos ocultos con:

```
ls -a
```

obsrervamos que tiene un control de versiones con git, vemos las versiones anteriroes del message.txt:

```
git log
```

Solo que cuenta con una cantidad enorme de commits, para resolverlo utilizamos:

```
git blame message.py
```

y encontramos la flag:

picoCTF{@sk_th3_1nt3rn_e9957ce1}
## NOTAS ADICIONALES

## REFERENCIAS



