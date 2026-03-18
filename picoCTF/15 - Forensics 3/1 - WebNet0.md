
## DESCRIPCIÓN
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/picopico.key). Recover the flag.
## SOLUCIÓN
Descargamos ambos archivos, si observamos el archivo de captura de paquetes vemos que esta esta encryptada en TLS, propio de HTTPS, entonces abrimos el archivo con wireshark y nos vamos a:

Edit -> Preferences -> Protocols -> TLS -> RSA KEY -> ADD -> FILE BROWSER -> PEGAMOS LA KEY -> 0K

Al aplicarla se desencriptan los paquetes, los de verde le ponemos al primero follow https y en el primero.

y obtenemos la flag:

picoCTF{nongshim.shrimp.crackers}

## NOTAS ADICIONALES
- Otra forma de hacerlo es con ssldump:

```
ssldump -r capture.pcap  -d -k picopico.key | grep picoCTF -A 2
```

Le pasamos el archivo, la llave y filtramos el picoCTF, el -A significa que tambien tome 2 lineas despues (After) por que la bandera aparece cortada.
## REFERENCIAS




