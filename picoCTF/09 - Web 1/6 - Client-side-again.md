
## DESCRIPCIÓN
Can you break into this super secure portal?

http://fickle-tempest.picoctf.net:61862
## SOLUCIÓN
Ingresamos al http desde el navegador de firefox, observamos el código de javascript, sin embargo este se encuentra "sofuscado" osea muy pegado y poco legible, con la ayuda de una pagina como jsnice lo hacemos mas legible y observamos el arreglo en donde se encuentran los pedazos de la flag:

```
var _0x5a46 = ["daf93}", "_again_4", "this", "Password Verified", "Incorrect password", "getElementById", "value", "substring", "picoCTF{", "not_this"];
```

Tan solo con pura lógica ordenamos los pedazos.

Y obtenemos la flag:

picoCTF{not_this_again_4daf93}
## NOTAS ADICIONALES

## REFERENCIAS
- http://jsnice.org/




