
## DESCRIPCIÓN
Using a Secure Shell (SSH) is going to be pretty important.

Additional details will be available after launching your challenge instance.

Can you `ssh` as `ctf-player` to `titan.picoctf.net` at port `54288` to get the flag?You'll also need the password `f3b61b38`. If asked, accept the fingerprint with `yes`.If your device doesn't have a shell, you can use: [https://webshell.picoctf.org](https://webshell.picoctf.org/)If you're not sure what a shell is, check out our Primer: [https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)
## SOLUCIÓN
En base a los datos proporcionados nos conectamos con la ayuda de ssh al servidor: 

```
ssh -p 54288 ctf-player@titan.picoctf.net
```

Una vez conectados, el mensaje de bienvenida incluye la flag:

picoCTF{s3cur3_c0nn3ct10n_3e293eea}
## NOTAS ADICIONALES

## REFERENCIAS



