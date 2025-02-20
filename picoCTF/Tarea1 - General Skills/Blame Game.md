Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/73/challenge.zip)

Hints:
- In collaborative projects, many users can make many changes. How can you see the changes within one file?
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
- You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge

Solución
Una vez entrando a la carpeta podemos usar el comando de git log para ver los commits hechos anteriormente. Analizando estos podemos ver que la flag está en el autor de uno de los commits iniciales
```
commit fadeca9476b6713ec8cdda633aca9e9aebffc698
Author: picoCTF{@sk_th3_1nt3rn_e9957ce1} <ops@picoctf.com>
Date:   Sat Mar 9 21:09:11 2024 +0000

    optimize file size of prod code
```