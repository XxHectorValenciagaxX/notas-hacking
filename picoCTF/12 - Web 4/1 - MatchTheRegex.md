
## DESCRIPCIÓN
How about trying to match a regular expression

The website is running [here](http://saturn.picoctf.net:64770/).
## SOLUCIÓN
Este reto usa de expresiones regulares, las cuales establecen una serie de caracteres a validar, si un texto de input cumple con la expresión, esta es válida.

Si vemos el código fuente obeservamos:

```
function send_request() {
		let val = document.getElementById("name").value;
		// ^p.....F!?
		fetch(`/flag?input=${val}`)
			.then(res => res.text())
			.then(res => {
				const res_json = JSON.parse(res);
				alert(res_json.flag)
				return false;
			})
		return false;
	}
```

Observamos que "^p.....F!?", entoces cualquier texto que inicie con p y termine con F (el ! es opcional) es valido.

y obtenemos la flag:

picoCTF{succ3ssfully_matchtheregex_08c310c6}
## NOTAS ADICIONALES

## REFERENCIAS





