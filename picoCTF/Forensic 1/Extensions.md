This is a really weird text file TXT? Can you find the flag?

Hints:
- How do operating systems know what kind of file it is? (It's not just the ending!
- Make sure to submit the flag as picoCTF{XXXXX}

# Solución
Si le hacemos un file al archivo flag.txt nos dice que es png:
```
┌──(diego㉿Tallin)-[~/pico/extensions]
└─$ file flag.txt     
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
```
Cambiamos la extensión para ver la imagen:
```
┌──(diego㉿Tallin)-[~/pico/extensions]
└─$ mv flag.txt flag.png
```
Al abrir la imagen vemos la flag:
```
picoCTF{now_you_know_about_extensions}
```