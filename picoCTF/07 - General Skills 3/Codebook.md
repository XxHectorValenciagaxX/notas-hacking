
## DESCRIPCIÓN
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)
## SOLUCIÓN
Primero descargamos el archivo de python:

```
wget https://artifacts.picoctf.net/c/3/code.py

wget https://artifacts.picoctf.net/c/3/codebook.txt
```

El archivo codebook.txt funge como una contraseña, esta debe de encontrarse en el mismo directorio que code.py, al ejecutarlo se desbloquea y nos da la flag:

```
python code.py
```

Al ejecutarlo se encuentra la flag:

picoCTF{c0d3b00k_455157_197a982c}
## NOTAS ADICIONALES

## REFERENCIAS



