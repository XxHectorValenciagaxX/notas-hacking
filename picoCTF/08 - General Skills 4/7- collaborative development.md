
## DESCRIPCIÓN
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/176/challenge.zip)
## SOLUCIÓN
Una vez descomprimido el archivo, nos ubicamos en la carpeta y al ser un trabajo en equipo observamos que existen varias ramas:

```
git branch -a
```

hay 3 ramas en total, nos ubicamos de una en una y obtenemos un  pedazo de la flag, por ejemplo con la rama 1 de 3:

```
git checkout feature/part-1

nano flag.py
```

y encontramos la flag:

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_2c91ca76}
## NOTAS ADICIONALES

## REFERENCIAS



