Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm) has extraordinarily helpful information...

Hints:
- This program will only work in the webshell or another Linux computer
- To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm`
- Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
- -h and --help are the most common arguments to give to programs to get more information from them!
- Not every program implements help features like -h and --help.

Solución 1 
Simplemente ejecutar el comando strings para imprimir los caracteres que se pueden imprimir del binario y filtrar con un grep la flag:
```
DiegoR09-picoctf@webshell:~/waveAFlag$ strings warm | grep "picoCTF"

Resultao:
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_f0668f62}
```

Solución 2
Darle permisos de ejecución al binario y al ejecutarlo pasarle el argumento -h:
```
DiegoR09-picoctf@webshell:~/waveAFlag$ chmod +x warm 

DiegoR09-picoctf@webshell:~/waveAFlag$ ./warm
Hello user! Pass me a -h to learn what I can do!

DiegoR09-picoctf@webshell:~/waveAFlag$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_f0668f62}
```