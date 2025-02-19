Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.

Hints:
- Does that encoding look familiar?
- The `str_xor` function does not need to be reverse engineered for this challenge.

Solución
Al entrar al código vemos que la contraseña que debemos de ingresar debe de ser igual a:
```
chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)
```
Con python podemos ejecutar eso y ver los valores de los hexadecimales:
```
>>> chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)
'de76'
```
Ejecutamos el programa, ingresamos la contraseña y vemos la flag:
```
DiegoR09-picoctf@webshell:~/PWCrack2$ python level2.py 
Please enter correct password for flag: de76

Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
```