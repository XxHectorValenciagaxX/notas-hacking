
## DESCRIPCIÓN
A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it?Download the message [here](https://artifacts.picoctf.net/c/190/message.txt).Put the decoded message in the picoCTF flag format, `picoCTF{decoded_message}`.
## SOLUCIÓN
Una vez descargado el archivo, buscamos algún decodificador de rail-fence y alli introducimos el mensaje, en key buscamos hasta que en decode se muestre un texto legible, en este caso seria key =4 y offset = 0.

y obtenemos la flag:

picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_D00AFDD3}

## NOTAS ADICIONALES

## REFERENCIAS
-  [https://cryptii.com/pipes/rail-fence-cipher/](https://cryptii.com/pipes/rail-fence-cipher/)





