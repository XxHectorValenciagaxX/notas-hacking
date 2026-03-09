
## DESCRIPCIÓN
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/134d2a2cf6ec5b7e757effc9b32977af7cc324b8e99a5ddb64737794a14dc18d/capture.pcap). 

Recover the flag.
## SOLUCIÓN
Descargamos la imagen con wget y vemos que este archivo es una captura de paquetes, ya han sido capturados, entonces usamos wireshark para observarlos:

```
wireshark capture.pcap
```

Entonces seleccionamos cualquier paquete UDP y le damos click derecho, le damos a follow, UDP stream, (esto hace que junte todos los paquetes del mismo tipo en un bloque, en streams), despues con las flechitas de la esquina inferior derecha en la parte 6 se encuentra la bandera ahi.

y obtenemos la flag:

picoCTF{StaT31355_636f6e6e}
## NOTAS ADICIONALES

## REFERENCIAS





