Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/60915/` ([link](https://jupiter.challenges.picoctf.org/problem/60915/)) or http://jupiter.challenges.picoctf.org:60915

Hints:
What part of the website could tell you where the creator doesn't want you to look?

Solución
Entrar a la ruta de robots.txt de la página
```
User-agent: *
Disallow: /8028f.html
```
A partir de esto entrar a esa ruta que nos muestra y observar la flag:
```
picoCTF{ca1cu1at1ng_Mach1n3s_8028f}
```
