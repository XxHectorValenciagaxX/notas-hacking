
## DESCRIPCIÓN
There is a nice program that you can talk to by using this command in a shell:

Additional details will be available after launching your challenge instance.

$ nc wily-courier.picoctf.net 51431, but it doesn't speak English...

## SOLUCIÓN
Al darle al launch instance, se activa el host de wily-courier.picoctf.net en el puerto 51431, nos conectamos con net cat y obtenemos una serie de números, como parecen ser solo números enteros, están codificados en ASCII, por lo que guardamos los números en un archivo .txt:

```
nc wily-courier.picoctf.net 51431 > response.txt
```

Una vez obtenemos los números solo queda traducirlos, con la ayuda del lenguaje awk (para analizar y procesar texto de forma masiva): 

```
awk '{printf "%c", $1}' response.txt
```
 
 y encontramos la flag:

picoCTF{g00d_k1tty!_n1c3_k1tty!_a94e7}

## NOTAS ADICIONALES

- Cuando una lista de números enteros tiene la secuencia que empieza en 112, 105, 99, 111 ... y termina en 125 es la estructura clásica de una flag de CTF que se encuentra en código ASCII.
## REFERENCIAS
