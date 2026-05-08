## DESCRIPCIÓN
Can you figure out how this program works to get the flag? Connect to the program with netcat: `$ nc saturn.picoctf.net 60144` The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV.c). 

The binary can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV).
## SOLUCIÓN
Descargamos el archivo binario y lo filtramos con el comando grep:

```
nm picker-IV | grep win
```

Y nos devuelve:

000000000040129e T win

Entonces solo tomamos los últimos números (40129e) los cuales son el hex clave que ingresaremos en el server con ayuda de netcat.

y obtenemos la flag:

picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}
## NOTAS ADICIONALES

## REFERENCIAS








