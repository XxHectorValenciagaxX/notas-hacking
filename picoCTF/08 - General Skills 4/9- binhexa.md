
## DESCRIPCIÓN
How well can you perfom basic binary operations?Start searching for the flag here

`nc titan.picoctf.net 50897`

## SOLUCIÓN
Una vez nos conectamos al servidor nos adentra en un juego de resolver operaciones con binarios: 

```
Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 10101010
Binary Number 2: 01110001


Question 1/6:
Operation 1: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 01010100
Incorrect. Try again
Enter the binary result: 101010100
Correct!

Question 2/6:
Operation 2: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 283

Incorrect input. Provide the right input
Enter the binary result: 01110001
Incorrect. Try again
Enter the binary result: 100011011
Correct!

Question 3/6:
Operation 3: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01110001
Incorrect. Try again
Enter the binary result: 11111011
Correct!

Question 4/6:
Operation 4: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10011 11010010

Incorrect input. Provide the right input
Enter the binary result: 100101100001010
Correct!

Question 5/6:
Operation 5: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00111000
Correct!

Question 6/6:
Operation 6: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00100000
Correct!

Enter the results of the last operation in hexadecimal: 20
```

Y obtenemos la flag:

picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d9a7ddd2}
## NOTAS ADICIONALES

## REFERENCIAS
- https://www.prepostseo.com/tool/binary-to-hex



