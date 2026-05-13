## DESCRIPCIÓN
What does asm1(0xe26) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/c7ce5cfbb522cd448de7adcb1dc42106af4f859002381aa47d85b45cc66aa3f2/test.S)
## SOLUCIÓN
Tenemos el siguiente archivo:

```
asm1:
	<+0>:	endbr32 
	<+4>:	push   ebp
	<+5>:	mov    ebp,esp
	<+7>:	cmp    DWORD PTR [ebp+0x8],0x75b
	<+14>:	jg     0x11d6 <asm1+41>
	<+16>:	cmp    DWORD PTR [ebp+0x8],0x34b
	<+23>:	jne    0x11ce <asm1+33>
	<+25>:	mov    eax,DWORD PTR [ebp+0x8]
	<+28>:	add    eax,0x13
	<+31>:	jmp    0x11ed <asm1+64>
	<+33>:	mov    eax,DWORD PTR [ebp+0x8]
	<+36>:	sub    eax,0x13
	<+39>:	jmp    0x11ed <asm1+64>
	<+41>:	cmp    DWORD PTR [ebp+0x8],0xe26
	<+48>:	jne    0x11e7 <asm1+58>
	<+50>:	mov    eax,DWORD PTR [ebp+0x8]
	<+53>:	sub    eax,0x13
	<+56>:	jmp    0x11ed <asm1+64>
	<+58>:	mov    eax,DWORD PTR [ebp+0x8]
	<+61>:	add    eax,0x13
	<+64>:	pop    ebp
	<+65>:	ret    


```

Revisamos línea por línea qué pasa con nuestro input `0xe26`. Lo primero que encontramos es una comparación contra `0x75b` con un salto `jg` (salta si es mayor). Como `0xe26` **sí es mayor** que `0x75b`, el salto **se toma** y brincamos directo a `<+41>`.

Ya en `<+41>`, nos encontramos otra comparación, ahora contra `0xe26` mismo, seguida de un `jne` (salta si son distintos). Como nuestro valor y el de la comparación son **exactamente iguales**, el salto **no se toma** y seguimos hacia abajo normalmente.

El flujo cae entonces en `<+50>`: mueve nuestro valor al registro principal (`mov eax, 0xe26`) y luego le resta `0x13` (`sub eax, 0x13`). Con eso, simplemente hacemos esa pequeña resta en hexadecimal (`0xe26 - 0x13 = 0xe13`), y ese resultado es el valor que la función retorna como flag.

Y obtenemos la flag:

0xe13
## NOTAS ADICIONALES

## REFERENCIAS








