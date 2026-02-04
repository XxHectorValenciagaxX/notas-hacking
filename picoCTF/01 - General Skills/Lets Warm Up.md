**DESCRIPCIÓN**

If i told you a word started with 0x70 in hexadecimal, what would it start with in ASCII

**SOLUCIÓN**

## Solución 1:

Convertir el número en hexadecimal a su representación en código ASCII

- Usar una herramienta web como cyberhef
## Solución 2:

- Puede usarse incluso el interprete de Python para convertir de hex a ascii

``` Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> int(0x70)
112
>>> chr(112)
'p'
>>> ord('p')
112
>>> 
```

picoCTF{p}

**NOTAS ADICIONALES**

**REFERENCIAS**
- [https://www.rapidtables.com/convert/number/hex-to-ascii.html](https://www.rapidtables.com/convert/number/hex-to-ascii.html)
- [https://gchg.github.io/CyberChef](https://gchg.github.io/CyberChef)
