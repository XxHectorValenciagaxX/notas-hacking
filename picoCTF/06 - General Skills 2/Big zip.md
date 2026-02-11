
## DESCRIPCIÓN
Unzip this archive and find the flag.
## SOLUCIÓN
Descargamos el archivo .zip

```
wget https://artifacts.picoctf.net/c/505/big-zip-files.zip
```

Después de descomprimirlo con unzip obtenemos una carpeta con muchos archivos .txt, es muy difícil buscar la flag de uno en uno, por lo que utilizamos la función de grep recursivamente para buscar en todos los archivos de esta carpeta:

```
grep -r pico .
```

Y entre tantos archivos encontramos la flag:

picoCTF{gr3p_15_m4g1c_ef8790dc}
## NOTAS ADICIONALES

## REFERENCIAS
- https://gemini.com


