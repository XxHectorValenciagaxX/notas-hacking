
## DESCRIPCIÓN
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.`ssh -p 59370 ctf-player@mimas.picoctf.net`Use password: `1db87a14`
## SOLUCIÓN
Entrar a la página dada y usar los comodines para poder acceder al .txt y conseguir la flag

- Primero es entrar al link que se nos da, después con ayuda de los comodines escribimos lo siguiente para poder acceder al .txt:

```
/???/???[!_]64 /????/??????????/??????/????????
```

- , con ese comando nos muestra un texto en base64 "cGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV83NzVhYzEyZH0=", que solo usamos cyberchef para transformarlo y obtenemos la flag

y obtenemos la flag:

picoCTF{7h15_mu171v3r53_15_m4dn355_4945630a}

## NOTAS ADICIONALES

## REFERENCIAS
- https://www.base64decode.org/



