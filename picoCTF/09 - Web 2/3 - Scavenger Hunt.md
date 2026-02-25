
## DESCRIPCIÓN
There is some interesting information hidden around this site. Can you find it?

http://wily-courier.picoctf.net:51147/
## SOLUCIÓN
Una vez ingresando en la pagina web, en el codigo fuente de html se encuentra la primera parte de la flag, (1/5), la segunda en el css, pero la tercera que deberia de encontrarse en el javascript, nos dice una pista:

How can I keep Google from indexing my website?

Y la respuesta es en el archivo de robots, para ello nos vamos a la url de:

http://wily-courier.picoctf.net:51147/robots.txt

Ahí mismo esta la pista para la siguiente parte:

I think this is an apache server... can you Access the next flag?

y la respuesta es en el archivo .htacess

http://wily-courier.picoctf.net:51147/.htaccess

la siguiente pista:

I love making websites on my Mac, I can Store a lot of information there.

y la respuesta es en el archivo .DS_Store (su equivalente en windows es .desktop.ini):

http://wily-courier.picoctf.net:51147/.DS_Store

Juntamos las partes y obtenemos la flag:

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_9588550}
## NOTAS ADICIONALES

## REFERENCIAS





