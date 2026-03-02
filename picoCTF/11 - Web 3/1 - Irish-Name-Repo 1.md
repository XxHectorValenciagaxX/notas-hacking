
## DESCRIPCIÓN
Do you think you can log us in? Try to see if you can login!

http://fickle-tempest.picoctf.net:57089.
## SOLUCIÓN
Una vez ingresado a la pagina en el login de admin, en el codigo fuente observamos:

```
<input type="hidden" name="debug" value="0">
```

quitamos el atributo hidden y el valor lo colocamos en 1, de esta forma nos muestra los resultados de depuracion:

username: 
password: 
SQL query: SELECT * FROM users WHERE name='' AND password=''

observamos que primero checa el nombre de usuario y luego la contraseña, se puede asumir que el nombre de usuario puede ser admin, entonces hacemos sqlinjection, escribimos en el label de admin:

admin' --    <-- Hay un espacio despues de --

de esa forma le indicamos que con que exista el usuario que ignore todo lo demas, incluyendo la contraseña. De esta forma al loguearse se la flag.

y obtenemos la flag:

picoCTF{s0m3_SQL_85832275}
## NOTAS ADICIONALES
- Otra forma de hacerlo es admin' or 1=1 --

- En terminal: 
```bash
curl http://fickle-tempest.picoctf.net:57728/login.php -d "username = admin' --  &password= loquesea&debug = 1"
```
## REFERENCIAS





