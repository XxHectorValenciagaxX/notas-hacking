
## DESCRIPCIÓN
Decode this [message](https://challenge-files.picoctf.net/c_fickle_tempest/c9834b19f74a20802d7c53dc42fe1ccd8a69da4cf5c38fa5b6aab8ec472efdd3/message.wav) from the moon.
## SOLUCIÓN
Descargamos el archivo llamado de audio y tambien descargamos una herramienta de decodificacion STTV:

```
cd /opt 

sudo git clone https://github.com/colaclanth/sstv 

cd sstv 

sudo python setup.py install
```

Nos ubicamos en la carpeta del archivo de audio y lo decodificamos:

```
sstv -d message.wav -o flag.png
```

Abrimos el flag.png con open.

y obtenemos la flag:

picoCTF{beep_boop_im_in_Space}

## NOTAS ADICIONALES

## REFERENCIAS
- https://stylesuxx.github.io/steganography/




