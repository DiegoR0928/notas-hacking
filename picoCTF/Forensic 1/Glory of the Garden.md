	This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.

Hints
What is a hex editor?

# Solución
Hacer un comando strings a la imagen y filtrar con grep para ver la flag
```
┌──(diego㉿Tallin)-[~/pico/gloryofthegarden]
└─$ strings  garden.jpg | grep "pico"
Here is a flag "picoCTF{more_than_m33ts_the_3y3657BaB2C}"
```
