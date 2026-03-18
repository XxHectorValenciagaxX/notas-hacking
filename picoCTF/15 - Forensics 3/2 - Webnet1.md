
## DESCRIPCIÓN
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/picopico.key). Recover the flag.
## SOLUCIÓN
Descargamos ambos archivos, si observamos el archivo de captura de paquetes vemos que esta esta encryptada en TLS, propio de HTTPS, entonces abrimos el archivo con wireshark y nos vamos a:

Edit -> Preferences -> Protocols -> TLS -> SKEY -> ADD -> FILE BROWSER -> PEGAMOS LA KEY -> 0K

Al aplicarla se desencriptan los paquetes, los de verde le ponemos al primero follow https y en el primero observamos que dice que esta ya no es tu bandera, por lo que nos vamos a:

FILE -> EXPORT OBJECT -> HTTP

Y observamos que alguien descargo una imagen, seleccionamos la imagen y le damos en save, y colocamos en la terminal:

```
strings vulture.jpg | grep picoCTF
```

y obtenemos la flag:

picoCTF{honey.roasted.peanuts}
## NOTAS ADICIONALES
- Otra forma de hacerlo es con ssldump:

```
ssldump -r capture.pcap -d picopico.key | grep picoCTF -A 
```

A final de cuentas la flag es un flujo de bits, aunque este en una imagen, por eso la puede extraer.
## REFERENCIAS




