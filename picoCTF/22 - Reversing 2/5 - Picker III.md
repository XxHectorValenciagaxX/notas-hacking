## DESCRIPCIÓN
Can you figure out how this program works to get the flag? Connect to the program with netcat: `$ nc saturn.picoctf.net 61521` The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/525/picker-III.py).
## SOLUCIÓN
Al descargar el código proporcionado, accedemos a la página indicada, después de analizar el código podemos observar que agregaron otra barrera que son las tablas ya definidas para las funciones, pero aprovechándonos de esto introducimos una función con las siguientes líneas, primero accedemos a la opción 3, luego "func_table" y por último, ingresamos:

```
"win' + ' ' * 125
```

Esto sobrescribe la tabla y coloca que en la primer función se ejecute el win al ejecutarla, para obtener el hexadecimal, y lo traducimos.

y obtenemos la flag:

picoCTF{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_a186f9ac}
## NOTAS ADICIONALES

## REFERENCIAS
[https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MCAweDY5IDB4NjMgMHg2ZiAweDQzIDB4NTQgMHg0NiAweDdiIDB4MzcgMHg2OCAweDMxIDB4MzUgMHg1ZiAweDMxIDB4MzUgMHg1ZiAweDc3IDB4NjggMHgzNCAweDM3IDB4NWYgMHg3NyAweDMzIDB4NWYgMHg2NyAweDMzIDB4MzcgMHg1ZiAweDc3IDB4MzEgMHgzNyAweDY4IDB4NWYgMHg3NSAweDM1IDB4MzMgMHg3MiAweDM1IDB4NWYgMHgzMSAweDZlIDB4NWYgMHg2MyAweDY4IDB4MzQgMHg3MiAweDY3IDB4MzMgMHg1ZiAweDYxIDB4MzEgMHgzOCAweDM2IDB4NjYgMHgzOSAweDYxIDB4NjMgMHg3ZA](https://gchq.github.io/CyberChef/#recipe=From_Hex\('Auto'\)&input=MHg3MCAweDY5IDB4NjMgMHg2ZiAweDQzIDB4NTQgMHg0NiAweDdiIDB4MzcgMHg2OCAweDMxIDB4MzUgMHg1ZiAweDMxIDB4MzUgMHg1ZiAweDc3IDB4NjggMHgzNCAweDM3IDB4NWYgMHg3NyAweDMzIDB4NWYgMHg2NyAweDMzIDB4MzcgMHg1ZiAweDc3IDB4MzEgMHgzNyAweDY4IDB4NWYgMHg3NSAweDM1IDB4MzMgMHg3MiAweDM1IDB4NWYgMHgzMSAweDZlIDB4NWYgMHg2MyAweDY4IDB4MzQgMHg3MiAweDY3IDB4MzMgMHg1ZiAweDYxIDB4MzEgMHgzOCAweDM2IDB4NjYgMHgzOSAweDYxIDB4NjMgMHg3ZA)







