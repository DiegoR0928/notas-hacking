Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance

Hints:
- ASCII is one of the most common encodings used in programming
- We know that the glitch output is valid Python, somehow!
- Press Ctrl and c on your keyboard to close your connection and return to the command promp

Solución
Imprimir el código de python que arroja una vez contectándose con netcat a saturn.picoctf.net 53300
```
print('picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}')

Resultado:
DiegoR09-picoctf@webshell:~$ python conversion.py

Resultado:
picoCTF{gl17ch_m3_n07_bda68f75}
```