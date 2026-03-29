
## DESCRIPCIÓN
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap) and try to get the flag.
## SOLUCIÓN
Descargamos el archivo de transmision de paquetes, lo abrimos con wireshark y lo picamos a la columna de Time para ordenarlos, ahi, nos centramos en todos los paquetes de len=12, seleccionamos uno por uno, le damos a la secicon de Retransmitted TCP segment data > le damos a Show Packets Bytes > ahi le damos a Decode as Base 64 y vamos copiando los pedazos de la flag, finalmente con todos de len=12 y un ultimo de len=4 que es la llave de cierre, los juntamos.

y obtenemos la flag:

picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3}

## NOTAS ADICIONALES

## REFERENCIAS



