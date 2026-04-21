
## DESCRIPCIÓN
In RSA, a small e value can be problematic, but what about N? Can you decrypt this?[values](https://challenge-files.picoctf.net/c_wily_courier/278a798f2fc4d2f3945588f28acb6f9a629b3eb05179b526e1de1bd3125b3c1b/values)
## SOLUCIÓN
Descargamos el archivo de values para conseguir los valores, después se puede observar que N es un número muy pequeño por lo que aprovechándonos de esto podemos obtener los valores de p y q para obtener la llave privada, después hacemos un código el cual se comunique con FactorDB.

```
import requests
import binascii

# Los datos de tu reto
c = 15341890103764929939105506004034128738090325640037083301857608662849501626260517
n = 948406957756830799684818171639547165784816468744946013083947881743680617123566349
e = 65537

print("[*] 1. Consultando a la API de FactorDB para romper N...")
# Hacemos una petición web a la base de datos
respuesta = requests.get(f"http://factordb.com/api?query={n}")
datos = respuesta.json()

# Si el status es 'FF', significa que FactorDB tiene todos los factores primos
if datos.get('status') == 'FF':
    # Extraemos los números primos. La API devuelve una lista de listas: [[factor, cantidad]]
    factores = [int(x[0]) for x in datos['factors']]

    if len(factores) >= 2:
        p = factores[0]
        q = factores[1]
        print(f"[+] ¡Factores encontrados al instante!\n    p = {p}\n    q = {q}")

        print("\n[*] 2. Reconstruyendo la llave privada (d)...")
        # Calculamos la función de Euler (totient)
        phi = (p - 1) * (q - 1)

        # Calculamos el inverso modular para obtener 'd'
        d = pow(e, -1, phi)
        print("[+] ¡Llave privada recreada con éxito!")

        print("\n[*] 3. Descifrando el mensaje...")
        # Aplicamos la fórmula matemática del descifrado: m = c^d mod n
        m = pow(c, d, n)

        # Formateamos el número gigante a texto legible (como en el reto anterior)
        hex_msg = hex(m)[2:]
        if len(hex_msg) % 2 != 0:
            hex_msg = "0" + hex_msg

        try:
            flag = binascii.unhexlify(hex_msg).decode('utf-8', errors='ignore')

            # ¡Invertimos la cadena para arreglar el Little-Endian!
            flag_corregida = flag[::-1]

            print(f"\n[🚀] FLAG: {flag_corregida}")
        except Exception as err:
            print(f"[-] Error al decodificar a texto: {err}")
```

y obtenemos la flag:

picoCTF{sma11_N_n0_g0od_1dc7ae91}
## NOTAS ADICIONALES

## REFERENCIAS







