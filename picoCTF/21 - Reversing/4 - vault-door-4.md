## DESCRIPCIÓN
This vault uses ASCII encoding for the password.The source code for this vault is here: [VaultDoor4.java](https://challenge-files.picoctf.net/c_fickle_tempest/5c887bc56d0c788895c28b80d7b702aff7b889fc7d8edf83fe0dc25c8aa11756/VaultDoor4.java)
## SOLUCIÓN
Descargamos el codigo que se nos proporciona, y en base a la logica del mismo podemos observar que la flag esta codificada por partes con distintas codificaciones, creamos un codigo en C# para traducirlo:

```
byte[] myBytes = { 106 , 85 , 53 , 116 , 95 , 52 , 95 , 98 , 0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f, 0142, 0131, 0164, 063 , 0163, 0137, 0145, 060 , '2' , '1' , '3' , '8' , '7' , '2' , '1' , '3' };
string decoded = System.Text.Encoding.ASCII.GetString(myBytes);
Console.WriteLine(decoded);
```

y obtenemos la flag:

picoCTF{jU5t_4_bUnCh_0f_bYt3s_0s_e021387213}

## NOTAS ADICIONALES

## REFERENCIAS
- https://gemini.google.com









