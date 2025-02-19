Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.

Hints
- To view the file in the webshell, do: `$ nano level1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

Solución
Entrar al código y observar que el input que espera como contraseña debe de ser igual a '691d', la ingresamos y obtenemos la flag:
```
DiegoR09-picoctf@webshell:~/PWCrack1$ python level1.py   
Please enter correct password for flag: 691d

Resultado:
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419};
```