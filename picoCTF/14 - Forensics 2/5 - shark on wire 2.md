
## DESCRIPCIÓN
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/07bf5ee832c595a6de406476b6c07f164d2951fbcfcf9cf3739c25dea26e5f0b/capture.pcap). Recover the flag.
## SOLUCIÓN
Descargamos el archivo de captura y al inspeccionarlo en wireshark, vemos que los flujos de paquetes UDP hay uno que dice start e inicia en el port 5000 y lo manda al 22, filtramos esos paquetes colocando en el filtro:

udp.dstport == 2

y al restarle 5000 a cada uno de los udp, por ejemplo el segundo que es de 5112. nos queda 112, si lo traducimos como char, nos da la palabra "p", y asi con cada uno obtenemos cada caracter de la flag.

Para automatizarlo creamos un archivo con nano llamado flag.py:

```
from scapy.all import * 

packets = rdpcap('capture.pcap')

flag='' 

for p in packets: 
	if UDP in p and p[UDP].dport == 22: 
		if p[UDP].sport > 5000: 
			flag+=chr(p[UDP].sport - 5000)
			
print(flag)
```

y obtenemos la flag:

picoCTF{p1LLf3r3d_data_v1a_st3g0}
## NOTAS ADICIONALES

## REFERENCIAS
- https://stylesuxx.github.io/steganography/




