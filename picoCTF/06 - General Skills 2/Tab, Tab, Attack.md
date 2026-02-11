
## DESCRIPCIÓN
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.
## SOLUCIÓN
Como nos tenemos que conectar a un servidor ssh y contamos tanto con el username, port y host, nos conectamos con el comando:

```
wget https://challenge-files.picoctf.net/c_wily_courier/c090282eec93405912f926586287741dd5b9bd24cbdf8f3555c53902d556e508/Addadshashanammu.zip
```

Al ejecutar dicho comando se nos descarga un archivo .zip, lo descomprimimos con el comando:

```
unzip Addadshashanammu.zip
```

Una vez descomprimido nos devuelve una serie de carpetas anidadas con nombres largos, por lo cual necesitaremos el tab para ubicarnos en ellas sin escribir su nombre completo, en un punto encontraremos un archivo .c y lo leemos con cat:

```
cat fang-of-haynekhtnamet.c
```

Al final se encuentra la flag:

picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
## NOTAS ADICIONALES
-  Lo ideal es ejecutar el programa ya que tiene un print que imprime la flag en la pantalla:

```
gcc fang-of-haynekhtnamet.c -o programa | ./programa
```

lo de programa es para que asi se llame el ejecutable resultante.
## REFERENCIAS
- https://itsfoss.com/es/escribir-compilar-ejecutar-programa-c-ubuntu/


