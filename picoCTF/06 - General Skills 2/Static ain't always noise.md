
## DESCRIPCIÓN
Can you look at the data in this binary? The bash script might help![static](https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/static), [ltdis.sh]

## SOLUCIÓN
Primero descargamos el file (warm) con el comando:

```
wget https://challenge-files.picoctf.net/c_wil
y_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/stat
ic | wget https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/ltdis.sh
```

Descargamos 2 archivos, un static y un archivo ltdis.sh, al observar el contenido (con cat) del ejecutable sh se puede observar que necesita de un criterio para desensamblarse, entonces lo hacemos ejecutable y lo ejecutamos con el argumento de static para desensamblarlo y extraer sus cadenas:

```
chmod +x ltdis.sh | ./ltdis.sh static
```

de esta forma obtenemos varios archivos .txt, uno de ellos es el que contiene las cadenas, solo queda buscar la flag:

```
grep pico static.ltdis.strings.txt
```

y obtenemos la flag:

picoCTF{d15a5m_t34s3r_20335e41}
## NOTAS ADICIONALES

## REFERENCIAS



