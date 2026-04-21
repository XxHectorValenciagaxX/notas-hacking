
## DESCRIPCIÓN
In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e?Connect with nc fickle-tempest.picoctf.net 58041.
## SOLUCIÓN
Accedemos al server con net cat y ahi se puede observar que la e en realidad es la d y termino cifrando con la llave privada, por lo que nos aprovechamos de esto y desciframos con 65537 la llave pública estándar.

```
import binascii

# Los datos de tu reto
c = 45089206614966215171799095611288356778494094665216741608385536419754124722701718932672648966183771297144350779352669761284575509423625027532323226197951604602553187400378591070067805195536309360398945118736495167308577204337408298944286097986500705475487042828335984849868495554720775987343880455491711382053
n = 122297454141675311544919767762431732212571232274289540658625439375207081244401230638968221882970360351973494162819829456924748464539099357577975088041363152769292576177658346327138491770706027446370329738377246177474100074458399982087756210653936122243579945837477396801053614271415723136216899924836704928127

# IGNORAMOS el 'e' gigante del reto.
# Usamos el valor por defecto estándar de RSA (2^16 + 1)
e_estandar = 65537

print("[*] Descifrando usando el 'e' por defecto (65537)...")

# Elevamos el texto cifrado al 'e' estándar, módulo n
m = pow(c, e_estandar, n)

# Convertimos a hexadecimal
hex_msg = hex(m)[2:]
if len(hex_msg) % 2 != 0:
    hex_msg = "0" + hex_msg

# Decodificamos a texto legible
try:
    flag = binascii.unhexlify(hex_msg).decode('utf-8')
    print(f"\n[🚀] FLAG: {flag}")
except Exception as err:
    print(f"[-] Error: {err}")
```

y obtenemos la flag:

picoCTF{bad_1d3a5_3801255}
## NOTAS ADICIONALES

## REFERENCIAS







