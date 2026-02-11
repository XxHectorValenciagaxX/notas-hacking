
## DESCRIPCIÓN
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?

Additional details will be available after launching your challenge instance.

Connect to fickle-tempest.picoctf.net 55577.

## SOLUCIÓN
Al conectarnos al servidor con el siguiente puerto:

```
nc fickle-tempest.picoctf.net 54437
```

Tenemos un tiempo límite para decodificar una serie de palabras, la primera de ellas esta en binario ("01110000 01101001 01100101"), con ayuda de una página de traducción obtenemos la palabra:

pie

después tenemos una codificación en octal (base 8): o143 o157 o155 o160 o165 o164 o145 o162 y se decodifica como:

computer

por último tenemos un código en hexadecimal que se transforma a ASCII (70656172):

pear

y una vez respondiéndolos correctamente obtenemos la flag:

picoCTF{learning_about_converting_values_DF19A0E8}

## NOTAS ADICIONALES

## REFERENCIAS
- https://traductorbinario.net/
- https://www.google.com/search?q=que+tipo+de+numero+es+o143+o157+o156+o164+o141+o151+o156+o145+o162&authuser=0&aep=21&udm=50&utm_source=google&utm_campaign=aim_aware&utm_content=oo-seaport-10855&mstk=AUtExfAdnplRQF1Gy0sfVBBXDKEuskr7zVMIzKqE-P_KSCeFg390wZH8l0oonKeZ3Ur_ni0CMa8qmuYcvJFfyMlG-rGPwV4NmQEfffEZzz4Tg5MS9qv2B3-ACR3_9xkdJfOaJxwOFrDqlty4v9kywqJrTEwJs18vXfCEpYMaYCXwhAZ6FLhX2F-p-wovHOtZeEz85v5ZXV0SoChuNyh7oRzi9s4oYVlWiaIQjFoOWNe8zaNZdjvBNVDMk8gPhB5jDJsTQtrFlK4NqA6GK687KNnIUtfVetCDOPcCdDnVqFgTSJbtYkhcsUCY4WhAeHfZLEb50w4TT2Z1Z0CwwQ&csuir=1&mtid=9juLaf23KffJwN4Ppt_wuAw

