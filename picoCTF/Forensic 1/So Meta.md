Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/00efdf2961da1e21470ffc0d496c3cc2/pico_img.png).

Hints
- What does meta mean in the context of files?
- Ever heard of metadata?

# Solución
Con un strings a la imagen y filtrar la flag con grep}
```
┌──(diego㉿Tallin)-[~/pico/soMeta]
└─$ strings pico_img.png | grep "picoCTF"
picoCTF{s0_m3ta_fec06741}
```

Ó con la aplicación exiftool en la parte del artista de la imagen
```
Artist                          : picoCTF{s0_m3ta_fec06741}
```

 