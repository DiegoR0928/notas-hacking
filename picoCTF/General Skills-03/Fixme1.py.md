Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)

Hints:
- Indentation is very meaningful in Python
- To view the file in the webshell, do: `$ nano fixme1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

Solución
Arreglar la indentación en una línea del código de python:
```
En esta linea:
print('That is correct! Here\'s your flag: ' + flag)
```
Y ejecutar el código:
```
DiegoR09-picoctf@webshell:~/fixme1$ python fixme1.py 

Resultado:
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
```