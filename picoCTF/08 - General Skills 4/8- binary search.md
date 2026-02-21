
## DESCRIPCIÓN
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/4/challenge.zip)

`ssh -p 64828 ctf-player@atlas.picoctf.net`Using the password `83dcefb7`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

## SOLUCIÓN
Una vez nos conectamos al servidor nos adentra en un juego de busqueda binaria, hay que encontrar el numero correcto de 1 en 1000 y tenemos 10 intentos, para ello empezamos con el 500 y nos dice si el numero es mas alto o mas bajo y tan solo vamos particionando el numero hasta encontrar el correcto:

```
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Lower! Try again.
Enter your guess: 625
Lower! Try again.
Enter your guess: 560
Higher! Try again.
Enter your guess: 595
Lower! Try again.
Enter your guess: 575
Lower! Try again.
Enter your guess: 568
Lower! Try again.
Enter your guess: 564
Lower! Try again.
Enter your guess: 562
Lower! Try again.
Enter your guess: 561
Congratulations! You guessed the correct number: 561
```

picoCTF{g00d_gu355_ee8225d0}
## NOTAS ADICIONALES

## REFERENCIAS



