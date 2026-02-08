
## DESCRIPCIÓN
Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way.The flag is in this [file](https://challenge-files.picoctf.net/c_fickle_tempest/d0b2e96347614d19414d591c946a1789fa8bd35487fcbfabf9437d0acfcaa503/file).

## SOLUCIÓN
Para encontrar una cadena de texto en un archivo, utilizamos grep para encontrar la flag desde linux, como sabemos de antemano como es la flag, utilizamos el siguiente comando:

```
grep CTF file.txt
```

y obtenemos la flag:

picoCTF{grep_is_good_to_find_things_e3C4b360}
## NOTAS ADICIONALES
- El carácter o cadena a buscar puede estar encerrado entre comillas o no.
## REFERENCIAS

