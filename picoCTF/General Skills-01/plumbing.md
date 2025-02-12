Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`

Hints: 
- Remember the flag format is picoCTF{XXXX}
- What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)

Solución
Utilizar pipelines para pasar el resultado de conectarse por netcat a `jupiter.challenges.picoctf.org 4427` a un grep y buscar por la cadena de la flag "picoCTF":
```
DiegoR09-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 4427 | grep "picoCTF"

Resultado:
picoCTF{digital_plumb3r_5ea1fbd7}
```