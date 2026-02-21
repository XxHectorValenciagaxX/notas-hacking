
## DESCRIPCIÓN
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.
`ssh -p 60197 ctf-player@saturn.picoctf.net`
The password is `8a707622`

## SOLUCIÓN
La shell especial modifica siempre la primera letra de los comandos a mayusculas, para ello hay que probar diferentes comandos:

```
`cat *`
```
descubrimos que blargh es un directorio entonces:

```
`cat blarch/*`
```

y encontramos la flag:

picoCTF{5p311ch3ck_15_7h3_w0r57_a60bdf40}
## NOTAS ADICIONALES
- Esta es otra forma de resolverlo:

```
INPUT             OUTPUT
${parameter=ls}	blargh
${parameter=cat blargh}	cat: blargh: Is a directory
${parameter=cd blargh}	${parameter=cd blargh}
${parameter=ls blargh}	flag.txt
${parameter=cat < blargh/flag.txt}	This gave the flag
```
## REFERENCIAS



