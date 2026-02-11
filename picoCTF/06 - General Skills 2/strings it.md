
## DESCRIPCIÓN
Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/563d66bbed3925c75ed71efa974bfafab26460ae99938d699a8881cd173fca60/strings) without running it?

## SOLUCIÓN
Primero descargamos el file con el comando:

```
wget https://challenge-files.picoctf.net/c_fickle_tempest/563d66bbed3925c75ed71efa974bfafab26460ae99938d699a8881cd173fca60/strings
```

Una vez obtenemos el archivo, este contiene mucho ruido, por lo que lo filtramos utilizando la funcion "strings" y el resultado lo guardamos:

```
strings strings > flag.txt
```

después buscamos la bandera dentro del filtrado:

```
grep pico flag.txt
```

y obtenemos la flag: 

picoCTF{5tRIng5_1T_dB2CEA76}
## NOTAS ADICIONALES
- La función strings sirve para extraer y mostrar secuencias de caracteres imprimibles, o sea, texto legible, incrustadas en archivos binarios, ejecutables o bibliotecas.

## REFERENCIAS
- https://www.google.com/search?q=para+que+funciona+la+funcion+strings+en+linux&rlz=1C1UEAD_esMX1072MX1072&oq=para+que+funciona+la+funcion+strings+en+linux&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRigATIHCAIQIRifBdIBCDY2MDhqMGo3qAIAsAIA&sourceid=chrome&ie=UTF-8


