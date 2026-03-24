
## DESCRIPCIÓN
🥛
## SOLUCIÓN
Ingresamos a la URL y vemos una imagen que parece ser un gif, le damos a alt + T y abrimos los tools, nos vamos a:

Tools > Page Info > Y descargamos la imagen, 

luego nos vamos a terminal y ponemos:

```
RUBY_THREAD_VM_STACK_SIZE=50000000 zsteg concat_v.png 
```

y obtenemos la flag:

picoCTF{imag3_m4n1pul4t10n_sl4p5}

## NOTAS ADICIONALES
- Por lo general basta con solo poner zsteg [nombre_imagen], sin embargo como era muy grande se coloca:
`
```
RUBY_THREAD_VM_STACK_SIZE=50000000 zsteg concat_v.png 
```

Para darle mas memoria de procesamiento y que lo pueda hacer.
## REFERENCIAS




