
## DESCRIPCIÓN
Additional details will be available after launching your challenge instance.

_debug info: [u:985978 e: p: c:34 i:297419]_

This challenge launches an instance on demand.  
Its current status is: `NOT_RUNNING`]

-UNA VEZ SE DIO A LAUNCH INSTANCE

Using netcat (nc) is going to be pretty important. Can you connect to fickle-tempest.picoctf.net at port 52561 to get the flag?

_debug info: [u:985978 e: p: c:34 i:297419]_

This challenge launches an instance on demand.  
Its current status is: `RUNNING`

## SOLUCIÓN
Al darle al launch instance, se activa el host de fickle-tempest.picoctf.net, con la ayuda del net cat, nos conectamos al puerto 52561, con el siguiente comando:

```
nc fickle-tempest.picoctf.net 52561
```

nos da un mensaje de animo y la siguiente flag:

picoCTF{nEtCat_Mast3ry_f20a728c}
## NOTAS ADICIONALES

## REFERENCIAS

