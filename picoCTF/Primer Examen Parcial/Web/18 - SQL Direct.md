
## DESCRIPCIÓN
Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 53858 -U postgres pico`Password is `postgres`
## SOLUCIÓN
Utilizar la webshell y usar la linea que se nos da con sus credenciales, después usando la terminal ir accediendo en pase a SQL postgres hasta conseguir la flag

- Primero es usar el webshell, después entramos con las credenciales que nos da, luego utilizamos \list para poder ver las distintas bases de datos que hay y usamos \c pico para entrar a la de pico, luego con \dt flags revisamos el esquema de las flags y por último usamos una sentencia sql "select * from flags;" para con ello obtener la flag

y obtenemos la flag:

picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}

## NOTAS ADICIONALES

## REFERENCIAS




