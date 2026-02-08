
## DESCRIPCIÓN
What is 0x3D (base 16) in decimal (base 10)?

## SOLUCIÓN
- Dicho numero a convertir es un numero hexadecimal (por defecto con base 16), utilizamos la misma pagina que con 2warm y colocamos from Hexadecimal to Decimal y como resultado da 61 (base por defecto 10), entonces la flag es: picoCTF{61}

- Otra solucion es utilizar python, en la terminal inicializamos la variable del hexadecimal como string y utilizando la funcion int( hexadecimal, 16) obtenemos el decimal:

```
>>> hex= "0x3D"
>>> r=int(hex,16)
>>> print(r)
61
```
## NOTAS ADICIONALES

## REFERENCIAS
- https://www.rapidtables.com/convert/number/decimal-to-binary.html?x=42

