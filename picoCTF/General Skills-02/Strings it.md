Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?

Hints:
	[strings](https://linux.die.net/man/1/strings)

Solución
Ejecutar el comando strings al archivo para que imprima los caracteres que se pueden imprimir y pasarlo a un grep con pipeline buscando el comienzo de la flag:
```bash
DiegoR09-picoctf@webshell:~/stringsIt$ strings strings | grep "picoCTF"

Resultado:
picoCTF{5tRIng5_1T_d66c7bb7}
```

