
## DESCRIPCIÓN
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/129/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## SOLUCIÓN
Una vez descargado el archivo, creamos un código en python para aplicar a los números un mod 37 e indicarle los caracteres permitidos.

```
numeros = [350, 63, 353, 198, 114, 369, 346, 184, 202, 322, 94, 235, 114, 110, 185, 188, 225, 212, 366, 374, 261, 213]

caracteres = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"

  

flag_interna = ""

for n in numeros:

    flag_interna += caracteres[n % 37]

  

print(f"picoCTF{{{flag_interna}}}")
```

y obtenemos la flag:

picoCTF{R0UND_N_R0UND_ADD17EC2}
## NOTAS ADICIONALES

## REFERENCIAS









