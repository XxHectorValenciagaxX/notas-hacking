
## DESCRIPCIÓN
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.`ssh -p 61383 ctf-player@saturn.picoctf.net`. The password is `af86add3`
## SOLUCIÓN
Entramos a la página dada y revisamos que podemos usar, aprovechando a ello usando read y echo vamos avanzando hasta obtener la flag

- Primero entramos a la página que se nos da con sus credenciales, después usamos un help para ver que comandos podemos usar, esta el echo y read, por lo que con "echo .* _/_" comprobamos las carpetas que hay y después con "echo "$(<file.txt)" vamos accediendo a los diferentes archivos hasta el de "ala/kazam.txt" con el que obtenemos la flag

y obtenemos la flag:

picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_a8567b6f}

## NOTAS ADICIONALES

## REFERENCIAS




