## DESCRIPCIÓN
What does asm3(0xb75a8f13,0xe1860bd7,0xc8e62f81) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/a8d942aa65a7a2dbe79352e0db95f90237024106f4efd380bda7ad339151b383/test.S)
## SOLUCIÓN
Tenemos el siguiente archivo:

```
asm3:
	<+0>:	endbr32 
	<+4>:	push   ebp
	<+5>:	mov    ebp,esp
	<+7>:	xor    eax,eax
	<+9>:	mov    ah,BYTE PTR [ebp+0x9]
	<+12>:	shl    ax,0x10
	<+16>:	sub    al,BYTE PTR [ebp+0xf]
	<+19>:	add    ah,BYTE PTR [ebp+0xd]
	<+22>:	xor    ax,WORD PTR [ebp+0x12]
	<+26>:	nop
	<+27>:	pop    ebp
	<+28>:	ret    


```

Revisamos línea por línea qué pasa con nuestros argumentos `0xb75a8f13, 0xe1860bd7, 0xc8e62f81`. Lo primero importante es recordar que x86 almacena los valores en **little-endian**, así que los bytes en memoria quedan así:

- `[ebp+0x8..0xb]` = `13 8f 5a b7`
- `[ebp+0xc..0xf]` = `d7 0b 86 e1`
- `[ebp+0x10..0x13]` = `81 2f e6 c8`

Arrancamos con `xor eax, eax`, que simplemente limpia el registro dejando `eax = 0`. Luego `mov ah, [ebp+0x9]` toma el byte en la posición `0x9`, que es `0x8f`, y lo mete en la parte alta de `ax`. Hasta aquí `ax = 0x8f00`.

Después viene `shl ax, 0x10`, un shift de 16 posiciones sobre un registro de 16 bits, lo que empuja todo fuera del registro dejando `ax = 0x0000`.

Ahora `sub al, [ebp+0xf]` resta el byte `0xe1` a `al` que vale `0x00`, con el wrap queda `al = 0x1f`. Luego `add ah, [ebp+0xd]` suma el byte `0x0b` a `ah` que vale `0x00`, quedando `ah = 0x0b`. En este punto `ax = 0x0b1f`.

Finalmente `xor ax, [ebp+0x12]` toma la word en `[ebp+0x12]` que es `0xc8e6` y hace el XOR: `0x0b1f XOR 0xc8e6 = 0xc3f9`. Ese valor se retorna en `eax`.

Y obtenemos la flag:

0xc3f9
## NOTAS ADICIONALES

## REFERENCIAS








