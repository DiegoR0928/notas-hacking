Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)

Hints
- Are equality and assignment the same symbol?
- To view the file in the webshell, do: `$ nano fixme2.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

Solución
Arreglar la síntaxis del archivo de python:
```
En esta linea, agregando un igual
if flag == "":
```
Y ejecutando el código:
```
DiegoR09-picoctf@webshell:~/fixme2$ python fixme2.py 

Resultado:
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```