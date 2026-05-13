## DESCRIPCIÓN
What does asm2(0xa,0x15) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/1b461fce4f77f2756ffeade3af119ec77d49db6fd9831387af61f9e3dec7a839/test.S)
## SOLUCIÓN
Tenemos el siguiente archivo:

```
asm2:
	<+0>:	endbr32 
	<+4>:	push   ebp
	<+5>:	mov    ebp,esp
	<+7>:	sub    esp,0x10
	<+10>:	mov    eax,DWORD PTR [ebp+0xc]
	<+13>:	mov    DWORD PTR [ebp-0x4],eax
	<+16>:	mov    eax,DWORD PTR [ebp+0x8]
	<+19>:	mov    DWORD PTR [ebp-0x8],eax
	<+22>:	jmp    0x11cd <asm2+32>
	<+24>:	add    DWORD PTR [ebp-0x4],0x1
	<+28>:	add    DWORD PTR [ebp-0x8],0x37
	<+32>:	cmp    DWORD PTR [ebp-0x8],0x84ab
	<+39>:	jle    0x11c5 <asm2+24>
	<+41>:	mov    eax,DWORD PTR [ebp-0x4]
	<+44>:	leave  
	<+45>:	ret   

```

Arrancamos con `[ebp-0x8] = 0xa` y `[ebp-0x4] = 0x15`. El loop corre mientras `[ebp-0x8] <= 0x84ab`, sumando `0x37` al contador principal y `0x1` al acumulador en cada vuelta. Cuando `[ebp-0x8]` finalmente supera `0x84ab`, la función mueve `[ebp-0x4]` a `eax` y retorna **`0x27f`**.

Y obtenemos la flag:

0x27f
## NOTAS ADICIONALES

## REFERENCIAS








