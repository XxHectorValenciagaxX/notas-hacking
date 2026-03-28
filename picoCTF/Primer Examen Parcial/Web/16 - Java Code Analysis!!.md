
## DESCRIPCIÓN
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/479/bookshelf-pico.zip).Website can be accessed [here!](http://saturn.picoctf.net:65328/).
## SOLUCIÓN
Entrar a la página y a la vez descargar el código que se nos da, conseguir las credenciales del JWT y acceder para conseguir la flag

- Primero es entrar a la página y conseguir allí el JWT que es para el usuario normal, después revisarlo con el decoder, luego de eso entramos al código, obtenemos el rol de Admin, el user id de 2 y el email de admin, además de la llave secreta que solamente es "1234", todo eso lo pasamos al encoder y conseguimos la nueva JWT de admin, después en la página editamos el almacenamiento local con el nuevo JWT y obtenemos la flag

y obtenemos la flag:

picoCTF{w34k_jwt_n0t_g00d_d7c2e335}

## NOTAS ADICIONALES

## REFERENCIAS
- https://www.jwt.io/



