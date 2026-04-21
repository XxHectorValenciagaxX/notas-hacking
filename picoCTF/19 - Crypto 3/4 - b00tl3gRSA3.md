
## DESCRIPCIÓN
Why use p and q when I can use more?Connect with nc fickle-tempest.picoctf.net 56362.
## SOLUCIÓN
Accedemos al server con net cat, pero antes de eso vemos la hint que nos dice que podemos usar más que solo p y q, lo que significa que la n está hecha de muchísimos números primos en lugar de solo dos. Por lo que nos apoyamos de la calculadora de Alpertron, pegamos la n gigante y nos arrojó 34 números primos distintos. Nos aprovechamos de esto y usamos esos 34 primos para calcular la función phi, reconstruimos la llave privada d y desciframos el mensaje original.

```
import binascii

  

# Datos

c = 12706662948698324542765700607828417973337912948403492191187201608331868946242338206875650140925821874614931158838326977144259695010171186772960393461094744086345043820733560286744225644656972933750247493532551583348809777863683798034190566282482288549413661787116132116515396680781014143885083467147530549393306865598292419283455044372907615704

n = 34459228071338679128076528615325666780043112470221745829313059985763927344670482536184127024009360939414223339188374211839377167448917269804255135576964368256678306527603247837852390562114149856109427942660781687905948870159631844063686872575148003895532663903998845181220087402944161783788423569526667280074173352179860160826613281747492634601

e = 65537

  

# Los 34 factores primos extraídos con Alpertron

factores = [

    8808096347, 8885025931, 9583479197, 10117791659, 10134033313,

    10238941199, 10384989959, 10412532829, 10424238421, 11179445231,

    11487789701, 11506506409, 11520711907, 12420981799, 12688545143,

    12783645247, 12839913011, 13115584021, 13312976731, 13495969999,

    13551358361, 13901984357, 14613128423, 14761351357, 14912800867,

    15106899503, 15160407061, 15339238823, 15574400767, 15706321511,

    15761095561, 15948239297, 16755533939, 17055296201

]

  

print(f"[*] Verificando {len(factores)} primos...")

  

# Calculamos la función Phi (Totient) para Multi-Prime

print("[*] Calculando Phi (Totient)...")

phi = 1

for primo in factores:

    phi *= (primo - 1)

  

# Reconstruimos la llave privada 'd'

print("[*] Reconstruyendo la llave privada (d)...")

d = pow(e, -1, phi)

  

# Desciframos el mensaje 'm'

print("[*] Descifrando el mensaje...")

m = pow(c, d, n)

  

# Formateamos a texto legible

hex_msg = hex(m)[2:]

if len(hex_msg) % 2 != 0:

    hex_msg = "0" + hex_msg

  

try:

    flag = binascii.unhexlify(hex_msg).decode('utf-8')

    print(f"\n[+] ¡Éxito!.")

    print(f"[🚀] FLAG: {flag}")

except Exception as err:

    print(f"[-] Error al decodificar: {err}")
```

y obtenemos la flag:

picoCTF{too_many_fact0rs_3023548}
## NOTAS ADICIONALES

## REFERENCIAS
- [https://www.alpertron.com.ar/ECM.HTM](https://www.alpertron.com.ar/ECM.HTM)







