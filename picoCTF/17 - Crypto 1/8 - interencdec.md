
## DESCRIPCIÓN
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/110/enc_flag).

## SOLUCIÓN
Obtenemos el texto codificado, en cyberchef lo desencryptamos con base64, el texto entre comillas lo copiamos y lo descencryptamos igual con bas64, finalmente obtenemos una codificacion en caesar, ponemos el ROT13 y vemos que en la rotacion 19 obtenemos la flag.

y obtenemos la flag:

picoCTF{caesar_d3cr9pt3d_86de32d2}
## NOTAS ADICIONALES

## REFERENCIAS
- https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,19)&input=d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg2a2wzMmsyfQoK






