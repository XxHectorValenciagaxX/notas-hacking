
## DESCRIPCIÓN
This service provides you an encrypted flag. Can you decrypt it with just N & e?Connect to the program with netcat:`$ nc verbal-sleep.picoctf.net 64446`The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/68dea6cb63f53886d85611943a2abf0c22e38ce960966417f393cd053daee689/encrypt.py).`
## SOLUCIÓN
Con la ayuda de FactorBD rompemos el RSA, primero entramos a la página que se nos indica para obtener los datos, después usando de nuevo FactorBD podemos simplemente conseguir los números primos y con ello ir haciendo los cálculos.

```
import requests

import binascii

  

# Los datos de tu reto

n = 24032504639261434860065343862682114133874996422566734467550449205101300294742546666515270769885898553643524769033907371922024097344575447760719921279681138

e = 65537

c = 9576510117436216480680440416531673628901497519262780055277158928904200567921668298246829409717936528495439019614213780801722818094700458007794409960714759

  

print("[*] Consultando FactorDB para romper N...")

respuesta = requests.get(f"http://factordb.com/api?query={n}")

datos = respuesta.json()

  

if datos.get('status') == 'FF':

    # Extraemos los primos automáticamente

    factores = [int(x[0]) for x in datos['factors']]

    print(f"[+] ¡Éxito! N está compuesto por {len(factores)} primos.")

  

    print("[*] Calculando Phi (Totient)...")

    phi = 1

    for primo in factores:

        phi *= (primo - 1)

  

    print("[*] Reconstruyendo la llave privada (d)...")

    d = pow(e, -1, phi)

  

    print("[*] Descifrando el mensaje...")

    m = pow(c, d, n)

  

    # Formateo a texto

    hex_msg = hex(m)[2:]

    if len(hex_msg) % 2 != 0:

        hex_msg = "0" + hex_msg

  

    try:

        flag = binascii.unhexlify(hex_msg).decode('utf-8')

        print(f"\n[🚀] FLAG: {flag}")

    except Exception as err:

        print(f"[-] Error al decodificar: {err}")

else:

    print("[-] FactorDB no lo tiene registrado. Pega el valor de N en Alpertron para factorizarlo manualmente.")
```

y obtenemos la flag:

picoCTF{tw0_1$_pr!m3df98b648}

## NOTAS ADICIONALES

## REFERENCIAS




