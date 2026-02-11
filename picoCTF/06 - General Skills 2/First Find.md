
## DESCRIPCIÓN
Unzip this archive and find the file named 'uber-secret.txt'
## SOLUCIÓN
Descargamos el archivo .zip

```
wget https://artifacts.picoctf.net/c/500/files.zip
```

Después de descomprimirlo con unzip y obtenemos una carpeta con varios archivos.

- LA PRIMERA FORMA DE RESOLVERLO:

Es buscando recursivamente la flag en cada archivo:

```
grep -r pico .
```

Y entre tantos archivos encontramos la flag:

picoCTF{f1nd_15_f457_ab443fd1}

- Otra forma es la forma "correcta / esperada" y es buscando el archivo uber-secret.txt, para ello utilizamos el siguiente comando, y una vez lo encuentra lo usa como argumento para leerlo con cat:

```
find -name uber-secret.txt | xargs cat
```

y encontramos la flag.
## NOTAS ADICIONALES
- xargs: Convierte la salida de un comando en un argumento para otro.
## REFERENCIAS
- https://gemini.com


