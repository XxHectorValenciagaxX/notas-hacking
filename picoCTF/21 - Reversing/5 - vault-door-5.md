## DESCRIPCIÓN
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding!The source code for this vault is here: [VaultDoor5.java](https://challenge-files.picoctf.net/c_fickle_tempest/aee691634d8cfd4a10820634bdea6b80aa104301e4b83d01fd4d176098d69e99/VaultDoor5.java)
## SOLUCIÓN
Descargamos el codigo que se nos proporciona, y en base a la logica del mismo podemos observar que la flag esta codificada en base 64 y en URL, tan solo lo traducimos con cyberchef

y obtenemos la flag:

picoCTF{c0nv3rt1ng_fr0m_ba5e_64_ed0b4288}

## NOTAS ADICIONALES

## REFERENCIAS
- https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)URL_Decode(true)&input=IkpUWXpKVE13SlRabEpUYzJKVE16SlRjeUpUYzBKVE14SlRabEpUWTNKVFZtIiAgICAgICAgICAgICAgICAgICAgICAgICJKVFkySlRjeUpUTXdKVFprSlRWbUpUWXlKVFl4SlRNMUpUWTFKVFZtSlRNMiIKIkpUTTBKVFZtSlRZMUpUWTBKVE13SlRZeUpUTTBKVE15SlRNNEpUTTQi










